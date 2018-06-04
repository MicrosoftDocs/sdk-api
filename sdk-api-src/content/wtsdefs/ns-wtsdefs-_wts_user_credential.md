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

# _WTS_USER_CREDENTIAL structure


## -description


Contains credential information for a user. This structure is used by the <a href="https://msdn.microsoft.com/48cd1a57-5f6d-4feb-889d-7441a76c0410">GetUserCredentials</a> method.


## -struct-fields




### -field UserName

A string that contains the name of the user.


### -field Password

A string that contains the user password.


### -field Domain

A string that contains the domain name for the user.


## -remarks



The user name and password are plaintext.



