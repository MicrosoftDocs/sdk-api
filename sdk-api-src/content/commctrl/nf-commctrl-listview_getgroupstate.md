---
UID: NF:commctrl.ListView_GetGroupState
title: ListView_GetGroupState macro
author: windows-sdk-content
description: Gets the state for a specified group. Use this macro or send the LVM_GETGROUPSTATE message explicitly.
old-location: controls\ListView_GetGroupState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupstate.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetGroupState, ListView_GetGroupState macro [Windows Controls], _shell_ListView_GetGroupState, _shell_ListView_GetGroupState_cpp, commctrl/ListView_GetGroupState, controls.ListView_GetGroupState, controls._shell_ListView_GetGroupState
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
 - ListView_GetGroupState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetGroupState macro


## -description


Gets the state for a specified group. Use this macro or send the <a href="https://msdn.microsoft.com/f087d17f-9066-44fb-b21b-ac7ceb56eb45">LVM_GETGROUPSTATE</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param dwGroupId [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the group by <b>iGroupId</b> (see  <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a> structure).


### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the state values to retrieve. This is a combination of the flags listed for the <b>state</b> member of <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>.

