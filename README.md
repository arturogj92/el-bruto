# ⚔️ EL BRUTO - Arena PvP

Juego de combate PvP estilo "My Brute" para jugar con amigos.

## Features

- 🎮 **PvP Matchmaking** - Combate automático entre jugadores de nivel similar
- ⚔️ **Combate directo** - Reta a cualquier jugador
- 🏟️ **Arena PvE** - Farmea XP contra NPCs (4 dificultades)
- 📈 **Progresión** - Sube de nivel, elige armas, habilidades o boosts
- 🎒 **Inventario** - Equipa hasta 4 armas, armadura y accesorio
- 🔓 **Sistema de Combos** - 16 combinaciones secretas de armas por descubrir
- 📖 **Libro de Combos** - Rastrea tus descubrimientos
- 👑 **Torneo Eliminatorio** - Cuando todos lleguen a nivel 20
- 📊 **Leaderboard** - Ranking por nivel y victorias
- 🎨 **Avatares IA** - Generados con Vertex AI Imagen

## Stack

- **Backend:** Express.js + SQLite (better-sqlite3)
- **Frontend:** Vanilla JS SPA
- **Combat Engine:** Sistema de turnos con habilidades, combos y efectos
- **Simulador de Balance:** 750K peleas para verificar equilibrio

## Setup

```bash
npm install
node server.js
```

El servidor arranca en el puerto 3485 por defecto.

## Balance Simulator

```bash
node simulate.js [ciclos] [partidas_por_par]
# Ejemplo: 5 ciclos de 10000 partidas
node simulate.js 5 10000
```

## API Endpoints

- `GET /api/players` - Lista jugadores
- `GET /api/player/:slug` - Detalle de jugador
- `POST /api/characters` - Crear personaje
- `POST /api/fight/matchmaking` - Matchmaking PvP
- `POST /api/fight/pvp` - Combate directo
- `POST /api/fight/pve` - Combate PvE
- `GET /api/combos` - Lista de combos de armas
- `GET /api/discoveries/:playerId` - Combos descubiertos
- `GET /api/leaderboard` - Ranking

## License

MIT
