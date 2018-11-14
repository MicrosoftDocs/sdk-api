---
UID: NF:commctrl.ListView_GetView
title: ListView_GetView macro
author: windows-sdk-content
description: Gets the current view of a list-view control. You can use this macro or send the LVM_GETVIEW message explicitly.
old-location: controls\ListView_GetView.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getview.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetView, ListView_GetView macro [Windows Controls], _win32_ListView_GetView, _win32_ListView_GetView_cpp, commctrl/ListView_GetView, controls.ListView_GetView, controls._win32_ListView_GetView
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
 - ListView_GetView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_GetView
: 
---

# ListView_GetView macro


## -description


Gets the current view of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761091(v=VS.85).aspx">LVM_GETVIEW</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_GetView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



