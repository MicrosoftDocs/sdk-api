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

# Edit_LineLength macro


## -description


Retrieves the length, in characters, of a line in an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/cfb0632c-9ba9-4864-939a-dbbaed6c177e">EM_LINELENGTH</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param line

Type: <b>int</b>

The zero-based index of the line.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/cfb0632c-9ba9-4864-939a-dbbaed6c177e">EM_LINELENGTH</a>.



