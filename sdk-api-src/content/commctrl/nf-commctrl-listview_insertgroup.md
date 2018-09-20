---
UID: NF:commctrl.ListView_InsertGroup
title: ListView_InsertGroup macro
author: windows-sdk-content
description: Inserts a group into a list-view control. You can use this macro or send the LVM_INSERTGROUP message explicitly.
old-location: controls\ListView_InsertGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertgroup.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ListView_InsertGroup, ListView_InsertGroup macro [Windows Controls], _win32_ListView_InsertGroup, _win32_ListView_InsertGroup_cpp, commctrl/ListView_InsertGroup, controls.ListView_InsertGroup, controls._win32_ListView_InsertGroup
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
 - ListView_InsertGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_InsertGroup macro


## -description


Inserts a group into a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/d43e21bc-e212-42dd-af88-48813d40cd50">LVM_INSERTGROUP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param index

Type: <b>int</b>


### -param pgrp

Type: <b>PLVGROUP</b>

<a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>

## -remarks



To turn on group mode, call <a href="https://msdn.microsoft.com/783a5e23-d1cb-4523-a6d2-b2cf93fa7f62">LVM_ENABLEGROUPVIEW</a> or <a href="https://msdn.microsoft.com/634066da-d82f-4612-bfce-64be6683465c">ListView_EnableGroupView</a>.


To use <b>ListView_InsertGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



