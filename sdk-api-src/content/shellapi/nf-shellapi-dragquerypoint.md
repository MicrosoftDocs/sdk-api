---
UID: NF:shellapi.DragQueryPoint
title: DragQueryPoint function
author: windows-driver-content
description: Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.
old-location: shell\DragQueryPoint.htm
old-project: shell
ms.assetid: 87794ab0-a075-4a1f-869f-5998bdc57a1d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DragQueryPoint, DragQueryPoint function [Windows Shell], _win32_DragQueryPoint, shell.DragQueryPoint, shellapi/DragQueryPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SHSTOCKICONID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	DragQueryPoint
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# DragQueryPoint function


## -description


Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.


## -parameters




### -param hDrop [in]

Type: <b>HDROP</b>

Handle of the drop structure that describes the dropped file.


### -param ppt

TBD




#### - lppt [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that, when this function returns successfully, receives the coordinates of the mouse pointer at the time the file was dropped.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the drop occurred in the client area of the window; otherwise <b>FALSE</b>.




## -remarks



The window for which coordinates are returned is the window that received the <a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> message.




## -see-also




<a href="https://msdn.microsoft.com/93fab381-9035-46c4-ba9d-efb2d0801d84">DragQueryFile</a>
 

 

