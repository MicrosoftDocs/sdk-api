---
UID: NF:commctrl.ListView_SetGroupState
title: ListView_SetGroupState macro
author: windows-sdk-content
description: Sets the state for a specified group.
old-location: controls\ListView_SetGroupState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_SetGroupState, ListView_SetGroupState macro [Windows Controls], _shell_ListView_SetGroupState, _shell_ListView_SetGroupState_cpp, commctrl/ListView_SetGroupState, controls.ListView_SetGroupState, controls._shell_ListView_SetGroupState
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
 - ListView_SetGroupState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetGroupState macro


## -description


Sets the state for a specified group.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param dwGroupId [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the group by <b>iGroupId</b> (see <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a> structure).


### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the state values to set or clear. This is a combination of the flags listed for the <b>state</b> member of <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>.


### -param dwState [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the state values to set. States that are not included here but are included in <i>dwMask</i> are cleared.


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>
You can also set the group state by using <a href="https://msdn.microsoft.com/97fb6a7e-9265-4faa-aab1-f45f87f4e76e">ListView_SetGroupInfo</a>.



