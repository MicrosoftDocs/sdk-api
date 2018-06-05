---
UID: NS:ntsecapi._KERB_CERTIFICATE_HASHINFO
title: "_KERB_CERTIFICATE_HASHINFO"
author: windows-sdk-content
description: Provides the payload information of the certificate hash.
old-location: security\kerb_certificate_hashinfo.htm
old-project: SecAuthN
ms.assetid: 09D78E91-5873-481D-A5FC-B7F39F8F9BB8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PKERB_CERTIFICATE_HASHINFO, KERB_CERTIFICATE_HASHINFO, KERB_CERTIFICATE_HASHINFO structure [Security], PKERB_CERTIFICATE_HASHINFO, PKERB_CERTIFICATE_HASHINFO structure pointer [Security], _KERB_CERTIFICATE_HASHINFO, ntsecapi/KERB_CERTIFICATE_HASHINFO, ntsecapi/PKERB_CERTIFICATE_HASHINFO, security.kerb_certificate_hashinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: KERB_CERTIFICATE_HASHINFO, *PKERB_CERTIFICATE_HASHINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	KERB_CERTIFICATE_HASHINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _KERB_CERTIFICATE_HASHINFO structure


## -description


The <b>KERB_CERTIFICATE_HASHINFO</b> structure provides the payload information of the certificate hash.


## -struct-fields




### -field StoreNameLength

Length, in bytes, of the WCHAR string specifying the certificate store name. If <b>StoreNameLength</b> is zero, the "MY" certificate store is implied; otherwise the WCHAR string must immediately follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure in contiguous memory and must include a terminating null character.



### -field HashLength

Length, in bytes, of the certificate hash. The certificate hash data must follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure and certificate store name (if present) in contiguous memory.


