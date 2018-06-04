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

# IBrowserService2::_SendChildren


## -description


Deprecated. Allows the derived class to send a message through the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> function directly instead of relying on the base class.


## -parameters




### -param hwndBar [in]

Type: <b>HWND</b>

A handle to the browser window whose window procedure receives the message.


### -param fBroadcast [in]

Type: <b>BOOL</b>


          The <b>BOOL</b> that indicates whether to allow the derived class to broadcast the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> function. <b>TRUE</b> to allow broadcasting; <b>FALSE</b> otherwise.
        


### -param uMsg [in]

Type: <b>UINT</b>

The message to be sent.


### -param wParam [in, out]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in, out]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



