---
UID: NS:mmc._SNodeID2
title: "_SNodeID2"
author: windows-sdk-content
description: The SNodeID2 structure is introduced in MMC 1.2, and replaces the SNodeID structure.
old-location: mmc\snodeid2.htm
old-project: mmc
ms.assetid: d7a0a5db-a84f-48f3-b1fb-5bccb104b62a
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: SNodeID2, SNodeID2 structure [MMC], _SNodeID2, _slate_snodeid2, mmc.snodeid2, mmc/SNodeID2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: SNodeID2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SNodeID2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SNodeID2 structure


## -description


The 
<b>SNodeID2</b> structure is introduced in MMC 1.2, and replaces the 
<a href="https://msdn.microsoft.com/aeaee0d8-7abf-4549-b184-326ab130fcb7">SNodeID</a> structure.

The 
<b>SNodeID2</b> structure is used by the 
<a href="https://msdn.microsoft.com/898f1691-6024-4873-a217-c8fb1b528400">CCF_NODEID2</a> clipboard format.

The 
<b>SNodeID2</b> structure contains an array of bytes that represent the node ID.


## -struct-fields




### -field dwFlags

Currently, only the MMC_NODEID_SLOW_RETRIEVAL flag is defined for <b>dwFlags</b>. If this flag is set, MMC will not persist the specified scope item except where absolutely necessary, as for example for console taskpads. Console taskpads always persist the target items and task target items.


### -field cBytes

The count of bytes in the <b>id</b> array.


### -field id

The bytes that contains the node ID of the scope item.


## -remarks



For details on using the 
<b>SNodeID2</b> structure with the CCF_NODEID2 clipboard format, see 
<a href="https://msdn.microsoft.com/898f1691-6024-4873-a217-c8fb1b528400">CCF_NODEID2</a>.




## -see-also




<a href="https://msdn.microsoft.com/898f1691-6024-4873-a217-c8fb1b528400">CCF_NODEID2</a>
 

 

