---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0030_0001
title: GPMBackupType (gpmgmt.h)
description: The type of backup created.
helpviewer_keywords: ["GPMBackupType","GPMBackupType enumeration [GPMC]","gpmc.gpmbackuptype","gpmgmt/GPMBackupType","gpmgmt/typeGPO","gpmgmt/typeStarterGPO","typeGPO","typeStarterGPO"]
old-location: gpmc\gpmbackuptype.htm
tech.root: gpmc
ms.assetid: 048871f3-39ea-4bf6-bc04-b4a34cd1a9d0
ms.date: 12/05/2018
ms.keywords: GPMBackupType, GPMBackupType enumeration [GPMC], gpmc.gpmbackuptype, gpmgmt/GPMBackupType, gpmgmt/typeGPO, gpmgmt/typeStarterGPO, typeGPO, typeStarterGPO
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
req.typenames: GPMBackupType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_gpmgmt_0000_0030_0001
 - gpmgmt/__MIDL___MIDL_itf_gpmgmt_0000_0030_0001
 - GPMBackupType
 - gpmgmt/GPMBackupType
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
 - GPMBackupType
---

# GPMBackupType enumeration


## -description

<b>GPMBackupType</b> defines the type of backup created.

<b>GPMBackupType</b> determines whether the backup is for a Group Policy object or a Starter Group Policy object.

```cpp
typedef enum {
    typeGPO = 0,
    typeStarterGPO
} GPMBackupType;
```

## -enum-fields

### -field typeGPO:0

Backup of a Group Policy object.

### -field typeStarterGPO

Backup of a Starter Group Policy object.

