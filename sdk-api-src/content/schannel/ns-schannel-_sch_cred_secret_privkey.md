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

# _SCH_CRED_SECRET_PRIVKEY structure


## -description


<p class="CCE_Message">[The <b>SCH_CRED_SECRET_PRIVKEY</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/8398e029-473e-488f-a861-c7ceae07e678">SCHANNEL_CRED</a> structure.]

The <b>SCH_CRED_SECRET_PRIVKEY</b> structure contains <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> information needed to authenticate a client or server.


## -struct-fields




### -field dwType

Must always be set to SCHANNEL_SECRET_PRIVKEY.


### -field pPrivateKey

Pointer to an encrypted private key.


### -field cbPrivateKey

Number of bytes in the encrypted private key.


### -field pszPassword

Pointer to a null-terminated string that Schannel uses to decrypt the private key.

