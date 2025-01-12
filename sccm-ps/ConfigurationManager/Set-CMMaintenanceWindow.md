---
description: Modifies a maintenance window.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMMaintenanceWindow
---

# Set-CMMaintenanceWindow

## SYNOPSIS
Modifies a maintenance window.

## SYNTAX

### ByValueMWValue (Default)
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -InputObject <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionId <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionId <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionName <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionName <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -InputObject <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMaintenanceWindow** cmdlet modifies a maintenance window associated with a collection.
Maintenance windows are periods of time reserved for write operations such as applying software updates, installing software, or configuring computer settings.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a maintenance window
```
PS XYZ:\> Set-CMMaintenanceWindow -Name "DiskCleanup"-CollectionID "AAA0004D" -ApplyToTaskSequenceOnly
```

This command modifies the maintenance window named DiskCleanup, a window associated with the collection AAA0004D.
In this example, the maintenance window is configured to apply only to task sequences.

## PARAMETERS

### -ApplyTo
```yaml
Type: MaintenanceWindowApplyTo
Parameter Sets: (All)
Aliases:
Accepted values: Any, SoftwareUpdatesOnly, TaskSequencesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToSoftwareUpdateOnly
Indicates that the maintenance window is used to apply software updates only.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToTaskSequenceOnly
Indicates that the maintenance window is used to apply task sequences only.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the collection that the maintenance window applies to.

```yaml
Type: String
Parameter Sets: ByCollectionIdMWName, ByCollectionIdMWValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionNameMWName, ByCollectionNameMWValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: ByValueMWValue, ByValueMWName
Aliases: Collection, Site

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsUtc
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindow
```yaml
Type: IResultObject
Parameter Sets: ByValueMWValue, ByCollectionIdMWValue, ByCollectionNameMWValue
Aliases: ScheduleWindow

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowName
Specifies the name of the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionIdMWName, ByCollectionNameMWName, ByValueMWName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

[New-CMMaintenanceWindow](New-CMMaintenanceWindow.md)

[New-CMSchedule](New-CMSchedule.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)
