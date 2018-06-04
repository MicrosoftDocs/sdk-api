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

# Edit_SetRectNoPaint macro


## -description


Sets the formatting rectangle of a multiline edit control. This macro is equivalent to <a href="https://msdn.microsoft.com/8778dcc9-51d0-4ab8-8fc1-2eebcdf12c35">Edit_SetRect</a>, except that it does not redraw the edit control window. You can use this macro or send the <a href="https://msdn.microsoft.com/1ab497ca-023f-4c26-b92d-b441a0d7b90c">EM_SETRECTNP</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the dimensions of the rectangle. If this parameter is <b>NULL</b>, the formatting rectangle is set to its default values. 


## -remarks



<b>Rich Edit 3.0 and later.</b> This macro does not have full functionality, because it does not set the WPARAM of the message.

For more information, see <a href="https://msdn.microsoft.com/1ab497ca-023f-4c26-b92d-b441a0d7b90c">EM_SETRECTNP</a>.



