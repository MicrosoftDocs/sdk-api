---
UID: NF:commctrl.ListView_SubItemHitTest
title: ListView_SubItemHitTest macro (commctrl.h)
description: Determines which list-view item or subitem is located at a given position. You can use this macro or send the LVM_SUBITEMHITTEST message explicitly.
helpviewer_keywords: ["ListView_SubItemHitTest","ListView_SubItemHitTest macro [Windows Controls]","_win32_ListView_SubItemHitTest","_win32_ListView_SubItemHitTest_cpp","commctrl/ListView_SubItemHitTest","controls.ListView_SubItemHitTest","controls._win32_ListView_SubItemHitTest"]
old-location: controls\ListView_SubItemHitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_subitemhittest.htm
ms.date: 12/05/2018
ms.keywords: ListView_SubItemHitTest, ListView_SubItemHitTest macro [Windows Controls], _win32_ListView_SubItemHitTest, _win32_ListView_SubItemHitTest_cpp, commctrl/ListView_SubItemHitTest, controls.ListView_SubItemHitTest, controls._win32_ListView_SubItemHitTest
f1_keywords:
- commctrl/ListView_SubItemHitTest
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SubItemHitTest macro


## -description


Determines which list-view item or subitem is located at a given position. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-subitemhittest">LVM_SUBITEMHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control that will be hit-tested. 


### -param plvhti

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvhittestinfo">LVHITTESTINFO</a> structure. The <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure within <b>LVHITTESTINFO</b> must be set to the client coordinates to be hit-tested. 

