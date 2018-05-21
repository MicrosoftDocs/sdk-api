---
UID: NF:commctrl.ListView_Scroll
title: ListView_Scroll macro
author: windows-driver-content
description: Scrolls the content of a list-view control. You can use this macro or send the LVM_SCROLL message explicitly.
old-location: controls\ListView_Scroll.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_scroll.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ListView_Scroll, ListView_Scroll macro [Windows Controls], _win32_ListView_Scroll, _win32_ListView_Scroll_cpp, commctrl/ListView_Scroll, controls.ListView_Scroll, controls._win32_ListView_Scroll
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
-	ListView_Scroll
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_Scroll macro


## -description


Scrolls the content of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/4bf6b74e-8fea-48ca-a151-8fd649fc50f8">LVM_SCROLL</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param dx

Type: <b>int</b>

A value of type <b>int</b> that specifies the amount of horizontal scrolling,  in pixels, relative to the current position of the list view content. If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column. 


### -param dy

Type: <b>int</b>

A value of type <b>int</b> that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



When the list-view control is in report view, the control can only be scrolled vertically in whole line increments. Therefore, the 
				<i>dy</i> parameter will be rounded to the nearest number of pixels that form a whole line increment. For example, if the height of a line is 16 pixels and 8 is passed for <i>dy</i>, the list will be scrolled by 16 pixels (1 line). If 7 is passed for <i>dy</i>, the list will be scrolled 0 pixels (0 lines). 



