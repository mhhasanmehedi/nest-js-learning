# Nest js

## For create module

```
npm g module users
```

## For create controller

```
npm g controller users
```

## For create service

```
npm g service users
```

### Users controller example

```
import { Controller, Get, Param } from '@nestjs/common';

@Controller('users')
export class UsersController {
  /**
   * GET /users
   * GET /users/:id
   * POST /users
   * PATCH /users/:id
   * DELETE /users/:id
   */

  @Get() // GET /users
  findAll() {
    return [];
  }

  @Get('interns') // GET /users/interns
  findAllInterns() {
    return [];
  }

  @Get(':id') // GET /users/:id
  findOne(@Param('id') id: string) {
    return {
      id,
    };
  }
}

```
