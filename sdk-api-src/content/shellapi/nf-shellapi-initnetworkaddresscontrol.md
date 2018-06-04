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

# InitNetworkAddressControl function


## -description


Initializes the network address control window class.


## -parameters






## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the initialization succeeded; or <b>FALSE</b> otherwise.




## -remarks



The network address control looks like an edit control and offers the additional functionality of network address verification. The control uses a balloon tip to display error messages.

This function initializes class WC_NETADDRESS. If this function returns <b>TRUE</b>, the control can be created.



