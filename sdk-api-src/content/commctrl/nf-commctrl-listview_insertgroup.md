---
UID: NF:commctrl.ListView_InsertGroup
title: ListView_InsertGroup macro
author: windows-sdk-content
description: Inserts a group into a list-view control. You can use this macro or send the LVM_INSERTGROUP message explicitly.
old-location: controls\ListView_InsertGroup.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertgroup.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_InsertGroup, ListView_InsertGroup macro [Windows Controls], _win32_ListView_InsertGroup, _win32_ListView_InsertGroup_cpp, commctrl/ListView_InsertGroup, controls.ListView_InsertGroup, controls._win32_ListView_InsertGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_InsertGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_InsertGroup macro


## -description


Inserts a group into a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761103(v=VS.85).aspx">LVM_INSERTGROUP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param index

Type: <b>int</b>


### -param pgrp

Type: <b>PLVGROUP</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a>

## -remarks



To turn on group mode, call <a href="https://msdn.microsoft.com/en-us/library/Bb774900(v=VS.85).aspx">LVM_ENABLEGROUPVIEW</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb761239(v=VS.85).aspx">ListView_EnableGroupView</a>.


To use <b>ListView_InsertGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



