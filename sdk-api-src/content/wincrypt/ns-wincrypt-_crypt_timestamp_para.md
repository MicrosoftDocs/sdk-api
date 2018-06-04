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

# _CRYPT_TIMESTAMP_PARA structure


## -description


The <b>CRYPT_TIMESTAMP_PARA</b> structure defines additional parameters for the time stamp request.


## -struct-fields




### -field pszTSAPolicyId

Optional. A pointer to a null-terminated character string that contains the Time Stamping Authority (TSA) policy under which the time stamp token
should be provided.


### -field fRequestCerts

A Boolean value that specifies whether the TSA must include the certificates
used to sign the time stamp token in the response .


### -field Nonce

Optional. A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available.


### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.


### -field rgExtension

A pointer to an array of <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures that contain extension information that is passed in the request.

