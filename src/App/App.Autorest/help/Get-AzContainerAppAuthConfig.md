---
external help file:
Module Name: Az.App
online version: https://learn.microsoft.com/powershell/module/az.app/get-azcontainerappauthconfig
schema: 2.0.0
---

# Get-AzContainerAppAuthConfig

## SYNOPSIS
Get a AuthConfig of a Container App.

## SYNTAX

### List (Default)
```
Get-AzContainerAppAuthConfig -ContainerAppName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Get
```
Get-AzContainerAppAuthConfig -ContainerAppName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzContainerAppAuthConfig -InputObject <IAppIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentityContainerApp
```
Get-AzContainerAppAuthConfig -ContainerAppInputObject <IAppIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Get a AuthConfig of a Container App.

## EXAMPLES

### Example 1: List AuthConfig of a Container App.
```powershell
Get-AzContainerAppAuthConfig -ContainerAppName azps-containerapp-2 -ResourceGroupName azps_test_group_app
```

```output
Name    PlatformEnabled ResourceGroupName
----    --------------- -----------------
current True            azps_test_group_app
```

List AuthConfig of a Container App.

### Example 2: Get a AuthConfig of a Container App.
```powershell
Get-AzContainerAppAuthConfig -ContainerAppName azps-containerapp-2 -ResourceGroupName azps_test_group_app -Name current
```

```output
Name    PlatformEnabled ResourceGroupName
----    --------------- -----------------
current True            azps_test_group_app
```

Get a AuthConfig of a Container App.

### Example 3: Get a AuthConfig of a Container App.
```powershell
$containerapp = Get-AzContainerApp -Name azps-containerapp-2 -ResourceGroupName azps_test_group_app
Get-AzContainerAppAuthConfig -ContainerAppInputObject $containerapp -Name current
```

```output
Name    PlatformEnabled ResourceGroupName
----    --------------- -----------------
current True            azps_test_group_app
```

Get a AuthConfig of a Container App.

## PARAMETERS

### -ContainerAppInputObject
Identity Parameter
To construct, see NOTES section for CONTAINERAPPINPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.App.Models.IAppIdentity
Parameter Sets: GetViaIdentityContainerApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ContainerAppName
Name of the Container App.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
The DefaultProfile parameter is not functional.
Use the SubscriptionId parameter when available if executing the cmdlet against a different subscription.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.App.Models.IAppIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name of the Container App AuthConfig.

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentityContainerApp
Aliases: AuthConfigName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group.
The name is case insensitive.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
The ID of the target subscription.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.App.Models.IAppIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.App.Models.IAuthConfig

## NOTES

## RELATED LINKS

