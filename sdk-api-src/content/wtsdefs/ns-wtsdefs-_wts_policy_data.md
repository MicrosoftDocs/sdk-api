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

# _WTS_POLICY_DATA structure


## -description


Contains policy information that is passed by the Remote Desktop Services service to the protocol.


## -struct-fields




### -field fDisableEncryption

Specifies whether to disable encryption for communication between the client and server.


### -field fDisableAutoReconnect

Specifies whether to disable automatic reconnect of the client.


### -field ColorDepth

Specifies the monitor color depth policy. This can be one of the following values.



#### 1

8 bits per pixel



#### 2

15 bits per pixel



#### 3

16 bits per pixel



#### 4

24 bits per pixel



#### 5

32 bits per pixel


### -field MinEncryptionLevel

Specifies the minimum permitted encryption level.


### -field fDisableCpm

Specifies whether to disable printer mapping.


### -field fDisableCdm

Specifies whether to disable drive mapping.


### -field fDisableCcm

Specifies whether to disable COM communication port mapping.


### -field fDisableLPT

Specifies whether to disable LPT (line print terminal) printer redirection.


### -field fDisableClip

Specifies whether to disable clipboard redirection.


### -field fDisablePNPRedir

Specifies whether to disable Plug and Play redirection.


## -remarks



This structure is used by the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fa77c537-c78d-4fe3-b597-787efd740cf6">GetUserData</a>
</li>
</ul>


