---
UID: NS:winuser.tagGESTURENOTIFYSTRUCT
title: tagGESTURENOTIFYSTRUCT
author: windows-sdk-content
description: When transmitted with WM_GESTURENOTIFY messages, passes information about a gesture.
old-location: wintouch\gesturenotifystruct.htm
old-project: wintouch
ms.assetid: e887c026-9300-4d20-8925-9939a664cd53
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*PGESTURENOTIFYSTRUCT, GESTURENOTIFYSTRUCT, GESTURENOTIFYSTRUCT structure [Windows Touch], PGESTURENOTIFYSTRUCT, PGESTURENOTIFYSTRUCT structure pointer [Windows Touch], tagGESTURENOTIFYSTRUCT, wintouch.gesturenotifystruct, winuser/GESTURENOTIFYSTRUCT, winuser/PGESTURENOTIFYSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: GESTURENOTIFYSTRUCT, *PGESTURENOTIFYSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - GESTURENOTIFYSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagGESTURENOTIFYSTRUCT structure


## -description



      When transmitted with <a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a> messages, 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a>
 

 

