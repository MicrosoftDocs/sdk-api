---
UID: NS:commctrl.tagLVITEMINDEX
title: tagLVITEMINDEX
author: windows-sdk-content
description: Contains index information about a list-view item.
old-location: controls\LVITEMINDEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvitemindex.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PLVITEMINDEX, LVITEMINDEX, LVITEMINDEX structure [Windows Controls], PLVITEMINDEX, PLVITEMINDEX structure pointer [Windows Controls], _shell_LVITEMINDEX, _shell_LVITEMINDEX_cpp, commctrl/LVITEMINDEX, commctrl/PLVITEMINDEX, controls.LVITEMINDEX, controls._shell_LVITEMINDEX, tagLVITEMINDEX"
ms.prod: windows-hardware
ms.technology: windows-devices
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



This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb774959(v=VS.85).aspx">ListView_GetItemIndexRect</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774986(v=VS.85).aspx">ListView_GetNextItemIndex</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb775097(v=VS.85).aspx">ListView_SetItemIndexState</a> macros. It is also used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761046(v=VS.85).aspx">LVM_GETITEMINDEXRECT</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761059(v=VS.85).aspx">LVM_GETNEXTITEMINDEX</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb761190(v=VS.85).aspx">LVM_SETITEMINDEXSTATE</a> messages.



