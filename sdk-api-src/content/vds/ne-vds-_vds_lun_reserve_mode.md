---
UID: NE:vds._VDS_LUN_RESERVE_MODE
title: "_VDS_LUN_RESERVE_MODE"
author: windows-sdk-content
description: Not supported.This enumeration is reserved for future use.
old-location: base\vds_lun_reserve_mode.htm
old-project: vds
ms.assetid: 198706a4-3692-4f75-bf68-c56671b752a5
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_LRM_EXCLUSIVE_RO, VDS_LRM_EXCLUSIVE_RW, VDS_LRM_NONE, VDS_LRM_SHARED_RO, VDS_LRM_SHARED_RW, VDS_LUN_RESERVE_MODE, VDS_LUN_RESERVE_MODE enumeration [VDS], _VDS_LUN_RESERVE_MODE, base.vds_lun_reserve_mode, vds/VDS_LRM_EXCLUSIVE_RO, vds/VDS_LRM_EXCLUSIVE_RW, vds/VDS_LRM_NONE, vds/VDS_LRM_SHARED_RO, vds/VDS_LRM_SHARED_RW, vds/VDS_LUN_RESERVE_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_LUN_RESERVE_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_LUN_RESERVE_MODE
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_LUN_RESERVE_MODE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Not supported.

This enumeration is reserved for future use.


## -enum-fields




### -field VDS_LRM_NONE

This value is reserved.


### -field VDS_LRM_EXCLUSIVE_RW

This value is reserved.


### -field VDS_LRM_EXCLUSIVE_RO

This value is reserved.


### -field VDS_LRM_SHARED_RO

This value is reserved.


### -field VDS_LRM_SHARED_RW

This value is reserved.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_RESERVE_MODE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_RESERVE_MODE</b> enumeration constant.</div>
<div> </div>


