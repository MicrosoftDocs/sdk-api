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

# IPSEC_AUTH_TYPE_ enumeration


## -description



		The <b>IPSEC_AUTH_TYPE</b> enumerated type indicates the type of hash algorithm used in an IPsec SA for data origin 
authentication and integrity protection.


## -enum-fields




### -field IPSEC_AUTH_MD5

Specifies MD5 hash algorithm. 

See <a href="Http://go.microsoft.com/fwlink/p/?linkid=84027">RFC 1321</a> for further information.


### -field IPSEC_AUTH_SHA_1

Specifies SHA 1 hash algorithm. 

See NIST, FIPS PUB 180-1 for more information.


### -field IPSEC_AUTH_SHA_256

Specifies SHA 256 hash algorithm.

See NIST, Draft FIPS PUB 180-2 for more information.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IPSEC_AUTH_AES_128

Specifies 128-bit AES hash algorithm.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IPSEC_AUTH_AES_192

Specifies 192-bit AES hash algorithm.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IPSEC_AUTH_AES_256

Specifies 256-bit AES hash algorithm.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IPSEC_AUTH_MAX

Maximum value for testing purposes.

