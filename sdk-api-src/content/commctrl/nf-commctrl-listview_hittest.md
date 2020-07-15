---
UID: NF:commctrl.ListView_HitTest
title: ListView_HitTest macro (commctrl.h)
description: Determines which list-view item, if any, is at a specified position. You can use this macro or send the LVM_HITTEST message explicitly.
helpviewer_keywords: ["ListView_HitTest","ListView_HitTest macro [Windows Controls]","_win32_ListView_HitTest","_win32_ListView_HitTest_cpp","commctrl/ListView_HitTest","controls.ListView_HitTest","controls._win32_ListView_HitTest"]
old-location: controls\ListView_HitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_hittest.htm
ms.date: 12/05/2018
ms.keywords: ListView_HitTest, ListView_HitTest macro [Windows Controls], _win32_ListView_HitTest, _win32_ListView_HitTest_cpp, commctrl/ListView_HitTest, controls.ListView_HitTest, controls._win32_ListView_HitTest
f1_keywords:
- commctrl/ListView_HitTest
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
- ListView_HitTest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_HitTest macro


## -description


Determines which list-view item, if any, is at a specified position. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-hittest">LVM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param pinfo

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvhittestinfo">LVHITTESTINFO</a> structure that contains the position to hit test and receives information about the results of the hit test. 

