---
UID: NF:commctrl.ListView_SetCheckState
title: ListView_SetCheckState macro
author: windows-sdk-content
description: Selects or deselects an item in a list-view control. You can use this macro or send the LVM_SETITEMSTATE message explicitly.
old-location: controls\ListView_SetCheckState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcheckstate.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ListView_SetCheckState, ListView_SetCheckState macro [Windows Controls], _win32_ListView_SetCheckState, _win32_ListView_SetCheckState_cpp, commctrl/ListView_SetCheckState, controls.ListView_SetCheckState, controls._win32_ListView_SetCheckState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
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
 - ListView_SetCheckState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetCheckState macro


## -description


Selects or deselects an item in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/aecd14dd-cfd0-4c7c-bddc-f65022de68c9">LVM_SETITEMSTATE</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param i

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the item for which to set the check state. 


### -param fCheck

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value that is set to <b>TRUE</b> to select the item, or <b>FALSE</b> to deselect it. 


## -remarks



This macro should only be used for list-view controls with the <a href="Extended_list_view_styles.htm">LVS_EX_CHECKBOXES</a> style. 




## -see-also




<a href="https://msdn.microsoft.com/b90900f1-833b-418c-8ddc-76c0743b77f9">ListView_SetItemState</a>
 

 

