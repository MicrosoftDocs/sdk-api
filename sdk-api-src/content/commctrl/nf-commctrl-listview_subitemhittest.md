---
UID: NF:commctrl.ListView_SubItemHitTest
title: ListView_SubItemHitTest macro
author: windows-sdk-content
description: Determines which list-view item or subitem is located at a given position. You can use this macro or send the LVM_SUBITEMHITTEST message explicitly.
old-location: controls\ListView_SubItemHitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_subitemhittest.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListView_SubItemHitTest, ListView_SubItemHitTest macro [Windows Controls], _win32_ListView_SubItemHitTest, _win32_ListView_SubItemHitTest_cpp, commctrl/ListView_SubItemHitTest, controls.ListView_SubItemHitTest, controls._win32_ListView_SubItemHitTest
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
 - ListView_SubItemHitTest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SubItemHitTest macro


## -description


Determines which list-view item or subitem is located at a given position. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761229(v=VS.85).aspx">LVM_SUBITEMHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control that will be hit-tested. 


### -param plvhti

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb774754(v=VS.85).aspx">LVHITTESTINFO</a> structure. The <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure within <b>LVHITTESTINFO</b> must be set to the client coordinates to be hit-tested. 

