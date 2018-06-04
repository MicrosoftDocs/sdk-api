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

# Edit_LineFromChar macro


## -description


Gets the index of the line that contains the specified character index in a multiline edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/e8e9217b-3f0c-478d-b44d-2a51868dbc5a">EM_LINEFROMCHAR</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param ich

Type: <b>int</b>

The zero-based index of the character from the beginning of the text in the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/e8e9217b-3f0c-478d-b44d-2a51868dbc5a">EM_LINEFROMCHAR</a>.



