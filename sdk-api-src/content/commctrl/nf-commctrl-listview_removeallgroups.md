---
UID: NF:commctrl.ListView_RemoveAllGroups
title: ListView_RemoveAllGroups macro (commctrl.h)
author: windows-sdk-content
description: Removes all groups from a list-view control. You can use this macro or send the LVM_REMOVEALLGROUPS message explicitly.
old-location: controls\ListView_RemoveAllGroups.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_removeallgroups.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_RemoveAllGroups, ListView_RemoveAllGroups macro [Windows Controls], _win32_ListView_RemoveAllGroups, _win32_ListView_RemoveAllGroups_cpp, commctrl/ListView_RemoveAllGroups, controls.ListView_RemoveAllGroups, controls._win32_ListView_RemoveAllGroups
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
 - ListView_RemoveAllGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_RemoveAllGroups macro


## -description


Removes all groups from a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761147(v=VS.85).aspx">LVM_REMOVEALLGROUPS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_RemoveAllGroups</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



