---
UID: NS:winuser.tagGESTURENOTIFYSTRUCT
title: GESTURENOTIFYSTRUCT (winuser.h)
description: When transmitted with WM_GESTURENOTIFY messages, passes information about a gesture.helpviewer_keywords: ["*PGESTURENOTIFYSTRUCT","GESTURENOTIFYSTRUCT","GESTURENOTIFYSTRUCT structure [Windows Touch]","PGESTURENOTIFYSTRUCT","PGESTURENOTIFYSTRUCT structure pointer [Windows Touch]","tagGESTURENOTIFYSTRUCT","wintouch.gesturenotifystruct","winuser/GESTURENOTIFYSTRUCT","winuser/PGESTURENOTIFYSTRUCT"]
old-location: wintouch\gesturenotifystruct.htm
tech.root: wintouch
ms.assetid: e887c026-9300-4d20-8925-9939a664cd53
ms.date: 12/05/2018
ms.keywords: '*PGESTURENOTIFYSTRUCT, GESTURENOTIFYSTRUCT, GESTURENOTIFYSTRUCT structure [Windows Touch], PGESTURENOTIFYSTRUCT, PGESTURENOTIFYSTRUCT structure pointer [Windows Touch], tagGESTURENOTIFYSTRUCT, wintouch.gesturenotifystruct, winuser/GESTURENOTIFYSTRUCT, winuser/PGESTURENOTIFYSTRUCT'
f1_keywords:
- winuser/GESTURENOTIFYSTRUCT
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- winuser.h
api_name:
- GESTURENOTIFYSTRUCT
targetos: Windows
req.typenames: GESTURENOTIFYSTRUCT, *PGESTURENOTIFYSTRUCT
req.redist: 
ms.custom: 19H1
---

# GESTURENOTIFYSTRUCT structure


## -description


When transmitted with <a href="https://docs.microsoft.com/windows/desktop/wintouch/wm-gesturenotify">WM_GESTURENOTIFY</a> messages, 
      passes information about a gesture.
  


## -struct-fields




### -field cbSize

The size of the structure.


### -field dwFlags

Reserved for future use.


### -field hwndTarget

The target window for the gesture notification.


### -field ptsLocation

The location of the gesture in physical screen coordinates.


### -field dwInstanceID

A specific gesture instance with gesture messages starting with <b>GID_START</b> and ending with <b>GID_END</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtstructures">Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/wm-gesturenotify">WM_GESTURENOTIFY</a>
 

 

