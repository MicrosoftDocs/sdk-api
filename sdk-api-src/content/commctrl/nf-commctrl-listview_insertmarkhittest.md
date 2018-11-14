---
UID: NF:commctrl.ListView_InsertMarkHitTest
title: ListView_InsertMarkHitTest macro
author: windows-sdk-content
description: Retrieves the insertion point closest to a specified point. You can use this macro or send the LVM_INSERTMARKHITTEST message explicitly.
old-location: controls\ListView_InsertMarkHitTest.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertmarkhittest.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_InsertMarkHitTest, ListView_InsertMarkHitTest macro [Windows Controls], _win32_ListView_InsertMarkHitTest, _win32_ListView_InsertMarkHitTest_cpp, commctrl/ListView_InsertMarkHitTest, controls.ListView_InsertMarkHitTest, controls._win32_ListView_InsertMarkHitTest
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
 - ListView_InsertMarkHitTest
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
- ListView_InsertMarkHitTest
: 
---

# ListView_InsertMarkHitTest macro


## -description


Retrieves the insertion point closest to a specified point. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761131(v=VS.85).aspx">LVM_INSERTMARKHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param point

Type: <b>LPPOINT</b>

<b>POINT</b>

### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774758(v=VS.85).aspx">LVINSERTMARK</a>
<i>point</i>

## -remarks



To use <b>ListView_InsertMarkHitTest</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



