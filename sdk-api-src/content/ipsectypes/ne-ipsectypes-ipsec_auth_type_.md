---
UID: NE:ipsectypes.IPSEC_AUTH_TYPE_
title: IPSEC_AUTH_TYPE_
author: windows-sdk-content
description: Indicates the type of hash algorithm used in an IPsec SA for data origin authentication and integrity protection.
old-location: fwp\ipsec_auth_type_enum.htm
tech.root: FWP
ms.assetid: 9130ffa3-b757-42fa-b6bb-d380f2dbdbcb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPSEC_AUTH_AES_128, IPSEC_AUTH_AES_192, IPSEC_AUTH_AES_256, IPSEC_AUTH_MAX, IPSEC_AUTH_MD5, IPSEC_AUTH_SHA_1, IPSEC_AUTH_SHA_256, IPSEC_AUTH_TYPE, IPSEC_AUTH_TYPE enumeration [Filtering], IPSEC_AUTH_TYPE_, fwp.ipsec_auth_type_enum, ipsectypes/IPSEC_AUTH_AES_128, ipsectypes/IPSEC_AUTH_AES_192, ipsectypes/IPSEC_AUTH_AES_256, ipsectypes/IPSEC_AUTH_MAX, ipsectypes/IPSEC_AUTH_MD5, ipsectypes/IPSEC_AUTH_SHA_1, ipsectypes/IPSEC_AUTH_SHA_256, ipsectypes/IPSEC_AUTH_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_AUTH_TYPE
product: Windows
targetos: Windows
req.typenames: IPSEC_AUTH_TYPE
req.redist: 
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

