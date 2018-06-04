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

# WPUPostMessage function


## -description



			The 
<b>WPUPostMessage</b> function performs the standard Windows <a href="_win32_postmessage_cpp">PostMessage</a> function in a way that maintains backward compatibility with older versions of WSOCK32.dll.


## -parameters




### -param hWnd [in]

Handle to the window that will receive the message.


### -param Msg [in]

Message that will be posted.


### -param wParam [in]

First parameter containing additional message-specific information.


### -param lParam [in]

Second parameter containing additional message-specific information.


## -returns




						If no error occurs, 
<b>WPUPostMessage</b> returns the <b>TRUE</b> value. Otherwise, the <b>FALSE</b> value is returned.



