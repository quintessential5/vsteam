---
external help file: VSTeam-Help.xml
Module Name: VSTeam
online version:
schema: 2.0.0
---

# Update-VSTeamTaskGroup

## SYNOPSIS

Updates an existing task group

## SYNTAX

## DESCRIPTION

Updates an existing task group

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------

```powershell

$projectName = "projectName"

$taskGroup = Get-VSTeamTaskGroup -Name "taskGroupName" -ProjectName $projectName

# Make some change, e.g.
$taskGroup.description = "new description"

$taskGroupJson = ConvertTo-Json -InputObject $taskGroup -Depth 10

Update-VSTeamTaskGroup -ProjectName $projectName -Id $taskGroup.id -Body $taskGroupJson
```

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Does not prompt

```yaml
Type: SwitchParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName

### -ProjectName

Specifies the team project for which this function operates.

You can tab complete from a list of available projects.

You can use Set-VSTeamDefaultProject to set a default project so
you do not have to pass the ProjectName with each call.

```yaml
Type: String
Position: 0
Required: True
Accept pipeline input: true (ByPropertyName)
```

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

ID of the existing task group

```yaml
Type: String
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InFile

The path to the json file that represents the task group

### -Body

The json that represents the task group as a string

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorTask, -InformationAction, -InformationTask, -OutTask, -OutBuffer, -PipelineTask, -Verbose, -WarningAction, and -WarningTask.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-VSTeamTaskGroup](Add-VSTeamTaskGroup.md)

[Get-VSTeamTaskGroup](Get-VSTeamTaskGroup.md)

[Remove-VSTeamTaskGroup](Remove-VSTeamTaskGroup.md)
