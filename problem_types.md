# Problem Types


## 🧩 Single-Agent Puzzles & Problems

| Puzzle / Problem                   | Solution Length  | Branching Factor | Complexity Class   | Search Required | Notes / Availability             |
| ---------------------------------- | ---------------- | ---------------- | ------------------ | --------------- | -------------------------------- |
| **Tower of Hanoi**                 | 2^N − 1          | 1                | Tractable          | No              | Classic recursive puzzle         |
| **River Crossing**                 | ∼4N              | >4               | NP-hard            | Yes             | Many Python examples             |
| **Blocks World**                   | ∼2N              | O(N²)            | PSPACE             | Yes             | In PDDL domains / Gym            |
| **Sliding Tile Puzzle (N-puzzle)** | O(N²)            | ≤4               | Exponential        | Yes             | `gymnasium` + `puzzle` libs      |
| **Rubik’s Cube (NxN)**             | O(N² log N)      | \~12–18          | Hard (EXP)         | Yes             | `pycuber`, `gym-rubik`           |
| **N-Queens**                       | O(N)             | N per row        | NP-complete        | Yes             | Simple backtracking code         |
| **Sudoku (NxN)**                   | N²               | up to N choices  | NP-complete        | Yes             | `pysudoku`, Python CSP           |
| **Lights Out**                     | ≤N²              | Grid-size        | P (linear algebra) | Sometimes       | Easy grid implementation         |
| **Peg Solitaire**                  | O(N²)            | O(N)             | Hard               | Yes             | Simple board sim                 |
| **Maze Navigation**                | O(N) path length | 4–8              | Depends on size    | Yes             | `gym-maze`, `minigrid`           |
| **TSP (Traveling Salesman)**       | N                | N!               | NP-hard            | Yes             | Many Python libs (e.g. OR-Tools) |
| **Graph Coloring**                 | N                | K                | NP-complete        | Yes             | NetworkX + search                |
| **SAT (k-SAT)**                    | N                | 2 per var        | NP-complete        | Yes             | `pycosat`, `z3`                  |
| **Minesweeper (NxN)**              | N²               | O(N²)            | NP-complete        | Yes             | Python + `gym-minesweeper`       |
| **Sokoban**                        | Exponential      | 4                | PSPACE-complete    | Yes             | `gym-sokoban`                    |

## 🤝 Multi-Agent Games & Problems

| Game / Problem                                     | Solution Length | Branching Factor | Complexity Class | Search Required | Notes / Availability        |
| -------------------------------------------------- | --------------- | ---------------- | ---------------- | --------------- | --------------------------- |
| **Chess (NxN)**                                    | O(N²)           | O(N²) moves      | PSPACE-hard      | Yes             | `python-chess`, `gym-chess` |
| **Go (NxN)**                                       | O(N²)           | O(N²)            | PSPACE-hard      | Yes             | `dlgo`, `gym-go`            |
| **Connect-K (generalized)**                        | O(N²)           | O(N)             | PSPACE-complete  | Yes             | Easy Python impl            |
| **Tic-Tac-Toe (N×N)**                              | O(N²)           | O(N)             | Easy             | No/Small Search | Tractable baseline          |
| **Generalized Nim**                                | O(N)            | O(N)             | Polynomial       | No              | Simple heap-game impl       |
| **Checkers (NxN)**                                 | O(N²)           | O(N)             | EXPTIME-complete | Yes             | Python libs exist           |
| **Multi-Agent Maze Chase (e.g. Pac-Man variants)** | Variable        | O(N)             | PSPACE           | Yes             | `gym-pacman`, PettingZoo    |
| **Multi-Agent Grid Soccer**                        | Variable        | O(N²)            | Hard             | Yes             | PettingZoo / RLLib Envs     |
| **Prisoner’s Dilemma (iterated)**                  | Fixed           | 2                | Easy             | No              | Simple payoff matrix        |
| **Stag Hunt / Coordination Games**                 | Fixed           | 2–3              | Easy             | No              | Matrix games or PettingZoo  |

## 🔧 Why These Are Useful

Systematic scaling → You can control difficulty by increasing N, board size, or #agents.

Clear complexity classes → From polynomial (easy) to NP-hard / PSPACE (hard).

Availability → Most already exist in Python via [Gymnasium](https://gymnasium.farama.org/)
, [PettingZoo](https://pettingzoo.farama.org/index.html)
, or small Python scripts.