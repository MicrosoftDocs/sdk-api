---
UID: NF:commctrl.ListView_InsertMarkHitTest
title: ListView_InsertMarkHitTest macro
author: windows-driver-content
description: Retrieves the insertion point closest to a specified point. You can use this macro or send the LVM_INSERTMARKHITTEST message explicitly.
old-location: controls\ListView_InsertMarkHitTest.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertmarkhittest.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_InsertMarkHitTest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_InsertMarkHitTest macro


## -description


Retrieves the insertion point closest to a specified point. You can use this macro or send the <a href="https://msdn.microsoft.com/901bb770-a36d-4d9f-a53b-d497b4df39e5">LVM_INSERTMARKHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param point

Type: <b>LPPOINT</b>

<b>POINT</b>

### -param lvim

TBD






#### - plvim

Type: <b>PLVINSERTMARK</b>

<a href="https://msdn.microsoft.com/61af07a1-34b1-4780-b36e-765e80783116">LVINSERTMARK</a>
<i>point</i>

## -remarks



To use <b>ListView_InsertMarkHitTest</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



