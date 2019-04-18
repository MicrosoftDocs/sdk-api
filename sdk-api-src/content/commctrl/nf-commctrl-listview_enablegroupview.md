---
UID: NF:commctrl.ListView_EnableGroupView
title: ListView_EnableGroupView macro (commctrl.h)
author: windows-sdk-content
description: Enables or disables whether the items in a list-view control display as a group. You can use this macro or send the LVM_ENABLEGROUPVIEW message explicitly.
old-location: controls\ListView_EnableGroupView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_enablegroupview.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_EnableGroupView, ListView_EnableGroupView macro [Windows Controls], _win32_ListView_EnableGroupView, _win32_ListView_EnableGroupView_cpp, commctrl/ListView_EnableGroupView, controls.ListView_EnableGroupView, controls._win32_ListView_EnableGroupView
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
 - ListView_EnableGroupView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_EnableGroupView macro


## -description


Enables or disables whether the items in a list-view control display as a group. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774900(v=VS.85).aspx">LVM_ENABLEGROUPVIEW</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param fEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>BOOL</b>
<b>TRUE</b>
<b>FALSE</b>

## -remarks



To use <b>ListView_EnableGroupView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



