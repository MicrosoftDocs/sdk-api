---
UID: NF:commctrl.ListView_ApproximateViewRect
title: ListView_ApproximateViewRect macro
author: windows-sdk-content
description: Calculates the approximate width and height required to display a given number of items. You can use this macro or send the LVM_APPROXIMATEVIEWRECT message explicitly.
old-location: controls\ListView_ApproximateViewRect.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_approximateviewrect.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ListView_ApproximateViewRect, ListView_ApproximateViewRect macro [Windows Controls], _win32_ListView_ApproximateViewRect, _win32_ListView_ApproximateViewRect_cpp, commctrl/ListView_ApproximateViewRect, controls.ListView_ApproximateViewRect, controls._win32_ListView_ApproximateViewRect
ms.prod: windows
ms.technology: windows-sdk
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
 - ListView_ApproximateViewRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_ApproximateViewRect macro


## -description


Calculates the approximate width and height required to display a given number of items. You can use this macro or send the <a href="https://msdn.microsoft.com/a14331a8-217d-48c6-9489-fb90c4d31b91">LVM_APPROXIMATEVIEWRECT</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iWidth

TBD


### -param iHeight

TBD


### -param iCount

Type: <b>int</b>

The number of items to be displayed in the control. If this parameter is -1, the message uses the total number of items in the control.


#### - cx

Type: <b>int</b>

The proposed x-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current width value. 


#### - cy

Type: <b>int</b>

The proposed y-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current height value. 


#### - hwndLV

Type: <b>hwndLV</b>

A handle to the list-view control. 

