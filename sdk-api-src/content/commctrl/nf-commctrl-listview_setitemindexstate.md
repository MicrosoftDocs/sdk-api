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


Sets the state of a specified list-view item. Use this macro or send the <a href="https://msdn.microsoft.com/9fea6420-320a-4d2a-84b5-7923fbb14655">LVM_SETITEMINDEXSTATE</a> message explicitly.


## -parameters




### -param hwndLV [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param plvii [in]

Type: <b><a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a> structure for the item. The caller is responsible for allocating this structure and setting the members.


### -param data [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The state to set on the item as one or more (as a bitwise combination) of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">List-View Item States</a> flags.


### -param mask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The valid bits of the state specified by parameter <i>data</i>. For more information, see the <i>stateMask</i> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a>) structure.

