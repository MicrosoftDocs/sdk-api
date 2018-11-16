---
UID: NF:commctrl.ListView_SortGroups
title: ListView_SortGroups macro
author: windows-sdk-content
description: Uses an application-defined comparison function to sort groups by ID within a list-view control. You can use this macro or send the LVM_SORTGROUPS message explicitly.
old-location: controls\ListView_SortGroups.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sortgroups.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ListView_SortGroups, ListView_SortGroups macro [Windows Controls], _win32_ListView_SortGroups, _win32_ListView_SortGroups_cpp, commctrl/ListView_SortGroups, controls.ListView_SortGroups, controls._win32_ListView_SortGroups
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
 - ListView_SortGroups
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
- ListView_SortGroups
: 
---

# ListView_SortGroups macro


## -description


Uses an application-defined comparison function to sort groups by ID within a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761225(v=VS.85).aspx">LVM_SORTGROUPS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param _pfnGroupCompate

Type: <b>PFNLVGROUPCOMPARE</b>


### -param _plv

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a></b>


## -remarks



To use <b>ListView_SortGroups</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



