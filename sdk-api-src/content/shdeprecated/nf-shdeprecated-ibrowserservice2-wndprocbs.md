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

# IBrowserService2::WndProcBS


## -description


Deprecated. Allows a derived class to call the <b>WinProc</b> function of the base class.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window receiving the message.


### -param uMsg [in]

Type: <b>UINT</b>

The message received by the window.


### -param wParam [in, out]

Type: <b>WPARAM</b>

Additional message information specific to the message type.


### -param lParam [in, out]

Type: <b>LPARAM</b>

Additional message information specific to the message type.


## -returns



Type: <b>LRESULT</b>

The return value specifies the result of the message processing; it depends on the message sent.



