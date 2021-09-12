# Entity Definition Update Manager

Provides developers with a class to perform automatic entity updates.

Use only in development environment.
Not to use on production websites.

## Support for automatic entity updates has been removed
https://www.drupal.org/node/3034742

User deprecated function: EntityDefinitionUpdateManagerInterface::applyUpdates() was deprecated in 8.7.0 and was removed before Drupal 9.0.0. Use \Drupal\Core\Entity\EntityDefinitionUpdateManagerInterface::getChangeList() and execute each entity type and field storage update manually instead.

### Entity Definition Update Manager
Customized class from the [Devel Entity Updates](https://www.drupal.org/project/devel_entity_updates) module
Development version of the entity definition update manager.


```
use Vardot\Entity\EntityDefinitionUpdateManager;
```

```
  // Entity updates to clear up any mismatched entity and/or field definitions
  // And Fix changes were detected in the entity type and field definitions.
  \Drupal::classResolver()
    ->getInstanceFromDefinition(EntityDefinitionUpdateManager::class)
    ->applyUpdates();
```
