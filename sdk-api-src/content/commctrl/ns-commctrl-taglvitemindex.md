---
UID: NS:commctrl.tagLVITEMINDEX
title: tagLVITEMINDEX
author: windows-sdk-content
description: Contains index information about a list-view item.
old-location: controls\LVITEMINDEX.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvitemindex.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PLVITEMINDEX, LVITEMINDEX, LVITEMINDEX structure [Windows Controls], PLVITEMINDEX, PLVITEMINDEX structure pointer [Windows Controls], _shell_LVITEMINDEX, _shell_LVITEMINDEX_cpp, commctrl/LVITEMINDEX, commctrl/PLVITEMINDEX, controls.LVITEMINDEX, controls._shell_LVITEMINDEX, tagLVITEMINDEX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVITEMINDEX
product: Windows
targetos: Windows
req.typenames: LVITEMINDEX, *PLVITEMINDEX
req.redist: 
---

# tagLVITEMINDEX structure


## -description


Contains index information about a list-view item.


## -struct-fields




### -field iItem

Type: <b>int</b>

The index of the item.


### -field iGroup

Type: <b>int</b>

The index of the group the item belongs to.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/eaf8e840-c057-41d4-bfc5-fdd66be8c6be">ListView_GetItemIndexRect</a>, <a href="https://msdn.microsoft.com/94a8e032-37c8-4ba0-99fe-6c2d77f0f2ee">ListView_GetNextItemIndex</a>, and <a href="https://msdn.microsoft.com/f1531cbd-d04a-4a12-9f29-d65122a1fb2c">ListView_SetItemIndexState</a> macros. It is also used with the <a href="https://msdn.microsoft.com/17704d24-c029-4d41-b198-04d1e78698e0">LVM_GETITEMINDEXRECT</a>, <a href="https://msdn.microsoft.com/84cfeb24-83b5-4028-a4ca-97c39ae3c817">LVM_GETNEXTITEMINDEX</a>, and <a href="https://msdn.microsoft.com/9fea6420-320a-4d2a-84b5-7923fbb14655">LVM_SETITEMINDEXSTATE</a> messages.



