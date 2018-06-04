---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ScrollBar_SetRange macro


## -description


Sets the range of a scroll bar.
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a> function, which is deprecated. New applications should use the <a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param posMin

Type: <b>int</b>

The minimum value of the scroll bar.


### -param posMax

Type: <b>int</b>

The maximum value of the scroll bar.


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to redraw the control; otherwise <b>FALSE</b>.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a>.



