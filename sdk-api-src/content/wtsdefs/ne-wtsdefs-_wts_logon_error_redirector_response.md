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

# _WTS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration


## -description


Contains values that specify the preferred response of the protocol to a logon error.


## -enum-fields




### -field WTS_LOGON_ERR_INVALID

This value is used for safe initialization.


### -field WTS_LOGON_ERR_NOT_HANDLED

Specifies that the client logon was not handled by the redirector and should be handled by the logon user interface.


### -field WTS_LOGON_ERR_HANDLED_SHOW

Specifies that the client logon was handled by the redirector and that the logon user interface should display itself normally.


### -field WTS_LOGON_ERR_HANDLED_DONT_SHOW

Specifies that the client logon was handled by the redirector and should not be passed to the next redirector. The logon user interface should not display an error message but should attempt to collect credentials again.


### -field WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER

Specifies that the client logon was handled by the redirector and should not be passed to the next redirector.  The logon user interface should not be displayed and should not attempt to collect credentials again.


## -remarks



This enumeration is used by the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/a333db5a-3564-4d33-bfd6-244975cc3c4f">RedirectStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8db3657c-f64f-4e38-832e-5808557f479d">RedirectMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10cd07c3-9617-4ef8-9b30-541a3206e7e4">RedirectLogonError</a>
</li>
</ul>


