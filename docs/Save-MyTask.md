---
external help file: MyTasks-help.xml
online version: 
schema: 2.0.0
---

# Save-MyTask
## SYNOPSIS
Archive completed or other tasks to a new file.

## SYNTAX

```
Save-MyTask [[-Path] <String>] [-Task <MyTask[]>] [-Passthru] [-WhatIf] [-Confirm]
```

## DESCRIPTION
Use this command to archive or save MyTask items to a new XML file.  They will be removed from the active XML source file. 

When you run the command by default all completed tasks will be removed from the tasks XML file and stored in a file called myTasksArchive.xml in the user's documents folder. You also have the option of archiving specific tasks. This will move the task to the new file in its current state. See examples.

This command has an alias of Archive-MyTask.

Note: Currently there are no commands in this module for working with the archived task XML file.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\> archive-mytask
```

Uaing the alias, archive all completed tasks to myTaskArchive.xml.

### -------------------------- EXAMPLE 2 --------------------------
```
PS C:\> get-mytask -Category other | save-mytask -Path c:\work\myOther.xml -Passthru


    Directory: C:\work


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        8/23/2016   9:55 AM            833 myOther.xml
```

Get all tasks in the Other category and save them to a new file. The tasks will be removed from the source file.
## PARAMETERS

### -Confirm

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -Passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path to a new XML file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -Task
A MyTask object.

```yaml
Type: MyTask[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WhatIf

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### MyTask[]

## OUTPUTS

### None

## NOTES

Learn more about PowerShell:
http://jdhitsolutions.com/blog/essential-powershell-resources/


## RELATED LINKS
[Get-MyTask]()
[Complete-MyTask]()
