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

# _WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description



Type for supplying a Windows credential as username, password, domain strings.
            


## -struct-fields




### -field credential


The base type from which this type and all other Windows Integrated
Authentication credential types derive.
                


### -field username


The username as a string.  This must be a valid user. To specify default credentials, use the WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL instead.


### -field password


The password for the username as a string.
                To specify a blank password, the length field of the string must be set to 0.


### -field domain


The domain name or the workgroup name as a string.
                

