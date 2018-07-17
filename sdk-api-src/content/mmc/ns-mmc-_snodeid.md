---
UID: NS:mmc._SNodeID
title: "_SNodeID"
author: windows-sdk-content
description: The SNodeID structure is introduced in MMC 1.1, and is replaced by the SNodeID2 structure in MMC 1.2.
old-location: mmc\snodeid.htm
old-project: mmc
ms.assetid: aeaee0d8-7abf-4549-b184-326ab130fcb7
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: SNodeID, SNodeID structure [MMC], _SNodeID, _slate_snodeid, mmc.snodeid, mmc/SNodeID
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
req.typenames: SNodeID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SNodeID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SNodeID structure


## -description


The 
<b>SNodeID</b> structure is introduced in MMC 1.1, and is replaced by the 
<a href="https://msdn.microsoft.com/d7a0a5db-a84f-48f3-b1fb-5bccb104b62a">SNodeID2</a> structure in MMC 1.2.

The 
<b>SNodeID</b> structure defines the format of the data for the 
<a href="https://msdn.microsoft.com/12c600c7-b904-4e7a-ae78-76e90de5e0aa">CCF_NODEID</a> clipboard format.

The 
<b>SNodeID</b> structure contains an array of bytes that represent the node ID.


## -struct-fields




### -field cBytes

The count of bytes in the <b>id</b> array.

The snap-in can also specify that a scope item should not be re-expanded when the console is reopened. To do this, set the <b>cBytes</b> member to 0 (zero) and return <b>S_OK</b> in the <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> method. Be aware that this setting not only keeps the selected item from being persisted but also prevents its parent item from automatically expanding when the console file is reopened.


### -field id

The bytes that contains the node ID of the scope item.


## -remarks



Your snap-in should support the <b>CCF_NODEID</b> clipboard format in its <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> method if any of its enumerated items has a volatile display name (such as the current computer name) or if any enumerated items should not be restored when the console file is reopened.

For details on using the 
<b>SNodeID</b> structure and <b>CCF_NODEID</b> clipboard format, see 
<a href="https://msdn.microsoft.com/12c600c7-b904-4e7a-ae78-76e90de5e0aa">CCF_NODEID</a>.




## -see-also




<a href="https://msdn.microsoft.com/12c600c7-b904-4e7a-ae78-76e90de5e0aa">CCF_NODEID</a>
 

 

