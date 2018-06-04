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

# Edit_Scroll macro


## -description


Scrolls the text vertically in a multiline edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97">EM_SCROLL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param dv

Type: <b>int</b>

The amount to scroll vertically.


### -param dh

Type: <b>int</b>

The amount to scroll horizontally.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97">EM_SCROLL</a>.



