---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0030_0001
title: "__MIDL___MIDL_itf_gpmgmt_0000_0030_0001"
author: windows-sdk-content
description: The type of backup created.
old-location: gpmc\gpmbackuptype.htm
old-project: GPMC
ms.assetid: 048871f3-39ea-4bf6-bc04-b4a34cd1a9d0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMBackupType, GPMBackupType enumeration [GPMC], __MIDL___MIDL_itf_gpmgmt_0000_0030_0001, gpmc.gpmbackuptype, gpmgmt/GPMBackupType, gpmgmt/typeGPO, gpmgmt/typeStarterGPO, typeGPO, typeStarterGPO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gpmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: GPMBackupType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gpmgmt.h
api_name:
 - GPMBackupType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_gpmgmt_0000_0030_0001 enumeration


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




### -field typeGPO

Backup of a Group Policy object.


### -field typeStarterGPO

Backup of a Starter Group Policy object.

