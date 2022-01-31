---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0000_0003
title: GPMSearchProperty (gpmgmt.h)
description: The property of the search criteria.
helpviewer_keywords: ["GPMSearchProperty","GPMSearchProperty enumeration [GPMC]","backupMostRecent","gpmc.gpmsearchproperty","gpmgmt/GPMSearchProperty","gpmgmt/backupMostRecent","gpmgmt/gpoComputerExtensions","gpmgmt/gpoDisplayName","gpmgmt/gpoDomain","gpmgmt/gpoEffectivePermissions","gpmgmt/gpoID","gpmgmt/gpoPermissions","gpmgmt/gpoUserExtensions","gpmgmt/gpoWMIFilter","gpmgmt/somLinks","gpmgmt/starterGPODisplayName","gpmgmt/starterGPODomain","gpmgmt/starterGPOEffectivePermissions","gpmgmt/starterGPOID","gpmgmt/starterGPOPermissions","gpoComputerExtensions","gpoDisplayName","gpoDomain","gpoEffectivePermissions","gpoID","gpoPermissions","gpoUserExtensions","gpoWMIFilter","somLinks","starterGPODisplayName","starterGPODomain","starterGPOEffectivePermissions","starterGPOID","starterGPOPermissions"]
old-location: gpmc\gpmsearchproperty.htm
tech.root: gpmc
ms.assetid: 9ac83c22-f253-449f-b639-b6a07e3c790b
ms.date: 12/05/2018
ms.keywords: GPMSearchProperty, GPMSearchProperty enumeration [GPMC], backupMostRecent, gpmc.gpmsearchproperty, gpmgmt/GPMSearchProperty, gpmgmt/backupMostRecent, gpmgmt/gpoComputerExtensions, gpmgmt/gpoDisplayName, gpmgmt/gpoDomain, gpmgmt/gpoEffectivePermissions, gpmgmt/gpoID, gpmgmt/gpoPermissions, gpmgmt/gpoUserExtensions, gpmgmt/gpoWMIFilter, gpmgmt/somLinks, gpmgmt/starterGPODisplayName, gpmgmt/starterGPODomain, gpmgmt/starterGPOEffectivePermissions, gpmgmt/starterGPOID, gpmgmt/starterGPOPermissions, gpoComputerExtensions, gpoDisplayName, gpoDomain, gpoEffectivePermissions, gpoID, gpoPermissions, gpoUserExtensions, gpoWMIFilter, somLinks, starterGPODisplayName, starterGPODomain, starterGPOEffectivePermissions, starterGPOID, starterGPOPermissions
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GPMSearchProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_gpmgmt_0000_0000_0003
 - gpmgmt/__MIDL___MIDL_itf_gpmgmt_0000_0000_0003
 - GPMSearchProperty
 - gpmgmt/GPMSearchProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gpmgmt.h
api_name:
 - GPMSearchProperty
---

# GPMSearchProperty enumeration


## -description

<b>GPMSearchProperty</b> defines  the property of the search criteria.

The property of the search criteria.

```cpp
typedef enum {gpoPermissions, gpoEffectivePermissions, gpoDisplayName, gpoWMIFilter, gpoID, 
              gpoComputerExtensions, gpoUserExtensions, somLinks, gpoDomain, backupMostRecent,
              starterGPOPermissions, starterGPOEffectivePermissions, starterGPODisplayName, starterGPOID,
              starterGPODomain} GPMSearchProperty;
```

## -enum-fields

### -field gpoPermissions:0

The specified level of permission for a Group Policy Object.

### -field gpoEffectivePermissions

A specific set of permissions, whether the permissions are explicitly set or derived as a result of group membership.

### -field gpoDisplayName

Display name of a Group Policy object.

### -field gpoWMIFilter

Display name of a WMI filter.

### -field gpoID

GUID of a Group Policy object.

### -field gpoComputerExtensions

Computer client-side extension

### -field gpoUserExtensions

user client-side extension

### -field somLinks

Scope of Management (SOM) that link to a Group Policy object.

### -field gpoDomain

domain name

### -field backupMostRecent

The most recent backup

### -field starterGPOPermissions

The specified level of permission for a Starter Group Policy Object.

### -field starterGPOEffectivePermissions

A specific set of permissions, whether the permissions are explicitly set or derived as a result of group membership.

### -field starterGPODisplayName

Display name of a Starter Group Policy object.

### -field starterGPOID

GUID of a Starter Group Policy object.

### -field starterGPODomain

domain name

