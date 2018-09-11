---
UID: NF:commctrl.ListView_SetItemIndexState
title: ListView_SetItemIndexState macro
author: windows-sdk-content
description: Sets the state of a specified list-view item. Use this macro or send the LVM_SETITEMINDEXSTATE message explicitly.
old-location: controls\ListView_SetItemIndexState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemindexstate.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_SetItemIndexState, ListView_SetItemIndexState macro [Windows Controls], _shell_ListView_SetItemIndexState, _shell_ListView_SetItemIndexState_cpp, commctrl/ListView_SetItemIndexState, controls.ListView_SetItemIndexState, controls._shell_ListView_SetItemIndexState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - ListView_SetItemIndexState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetItemIndexState macro


## -description


Sets the state of a specified list-view item. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761190(v=VS.85).aspx">LVM_SETITEMINDEXSTATE</a> message explicitly.


## -parameters




### -param hwndLV [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control.


### -param plvii [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774762(v=VS.85).aspx">LVITEMINDEX</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb774762(v=VS.85).aspx">LVITEMINDEX</a> structure for the item. The caller is responsible for allocating this structure and setting the members.


### -param data [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The state to set on the item as one or more (as a bitwise combination) of the <a href="https://msdn.microsoft.com/en-us/library/Bb774733(v=VS.85).aspx">List-View Item States</a> flags.


### -param mask [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The valid bits of the state specified by parameter <i>data</i>. For more information, see the <i>stateMask</i> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb774760(v=VS.85).aspx">LVITEM</a>) structure.

