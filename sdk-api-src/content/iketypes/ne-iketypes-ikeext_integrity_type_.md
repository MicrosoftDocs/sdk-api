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

# IKEEXT_INTEGRITY_TYPE_ enumeration


## -description



		The <b>IKEEXT_INTEGRITY_TYPE</b> enumerated type specifies the type of hash algorithm used for integrity protection of Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.


## -enum-fields




### -field IKEEXT_INTEGRITY_MD5

Specifies MD5 hash algorithm.


### -field IKEEXT_INTEGRITY_SHA1

Specifies SHA1 hash algorithm.


### -field IKEEXT_INTEGRITY_SHA_256

Specifies a 256-bit SHA encryption.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_INTEGRITY_SHA_384

Specifies a 384-bit SHA encryption.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_INTEGRITY_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

