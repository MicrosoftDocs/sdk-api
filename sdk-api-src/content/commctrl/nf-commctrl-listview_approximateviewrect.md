---
UID: NF:commctrl.ListView_ApproximateViewRect
title: ListView_ApproximateViewRect macro (commctrl.h)
author: windows-sdk-content
description: Calculates the approximate width and height required to display a given number of items. You can use this macro or send the LVM_APPROXIMATEVIEWRECT message explicitly.
old-location: controls\ListView_ApproximateViewRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_approximateviewrect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_ApproximateViewRect, ListView_ApproximateViewRect macro [Windows Controls], _win32_ListView_ApproximateViewRect, _win32_ListView_ApproximateViewRect_cpp, commctrl/ListView_ApproximateViewRect, controls.ListView_ApproximateViewRect, controls._win32_ListView_ApproximateViewRect
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_ApproximateViewRect"
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
 - ListView_ApproximateViewRect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_ApproximateViewRect macro


## -description


Calculates the approximate width and height required to display a given number of items. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-approximateviewrect">LVM_APPROXIMATEVIEWRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b>hwndLV</b>

A handle to the list-view control. 


### -param iWidth

Type: <b>int</b>

The proposed x-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current width value. 


### -param iHeight

Type: <b>int</b>

The proposed y-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current height value. 


### -param iCount

Type: <b>int</b>

The number of items to be displayed in the control. If this parameter is -1, the message uses the total number of items in the control.

