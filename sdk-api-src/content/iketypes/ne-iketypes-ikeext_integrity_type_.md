---
UID: NE:iketypes.IKEEXT_INTEGRITY_TYPE_
title: IKEEXT_INTEGRITY_TYPE_
author: windows-sdk-content
description: Specifies the type of hash algorithm used for integrity protection of Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.
old-location: fwp\ikeext_integrity_type.htm
old-project: FWP
ms.assetid: f4a5b6b9-5cf1-48a4-811c-9150550688d8
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IKEEXT_INTEGRITY_MD5, IKEEXT_INTEGRITY_SHA1, IKEEXT_INTEGRITY_SHA_256, IKEEXT_INTEGRITY_SHA_384, IKEEXT_INTEGRITY_TYPE, IKEEXT_INTEGRITY_TYPE enumeration [Filtering], IKEEXT_INTEGRITY_TYPE_, IKEEXT_INTEGRITY_TYPE_MAX, fwp.ikeext_integrity_type, iketypes/IKEEXT_INTEGRITY_MD5, iketypes/IKEEXT_INTEGRITY_SHA1, iketypes/IKEEXT_INTEGRITY_SHA_256, iketypes/IKEEXT_INTEGRITY_SHA_384, iketypes/IKEEXT_INTEGRITY_TYPE, iketypes/IKEEXT_INTEGRITY_TYPE_MAX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IKEEXT_INTEGRITY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_INTEGRITY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

