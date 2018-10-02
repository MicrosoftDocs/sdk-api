---
UID: NF:commctrl.ListView_SetGroupState
title: ListView_SetGroupState macro
author: windows-sdk-content
description: Sets the state for a specified group.
old-location: controls\ListView_SetGroupState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupstate.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control.


### -param dwGroupId [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the group by <b>iGroupId</b> (see <a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a> structure).


### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the state values to set or clear. This is a combination of the flags listed for the <b>state</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a>.


### -param dwState [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Specifies the state values to set. States that are not included here but are included in <i>dwMask</i> are cleared.


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>
You can also set the group state by using <a href="https://msdn.microsoft.com/en-us/library/Bb775079(v=VS.85).aspx">ListView_SetGroupInfo</a>.



