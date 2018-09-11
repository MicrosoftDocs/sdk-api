---
UID: NS:wincrypt._OCSP_REQUEST_ENTRY
title: "_OCSP_REQUEST_ENTRY"
author: windows-sdk-content
description: Contains information about a single certificate in an online certificate status protocol (OCSP) request.
old-location: security\ocsp_request_entry.htm
tech.root: seccrypto
ms.assetid: 61d5cbc9-22de-4768-b610-138bcd3c9cce
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*POCSP_REQUEST_ENTRY, OCSP_REQUEST_ENTRY, OCSP_REQUEST_ENTRY structure [Security], POCSP_REQUEST_ENTRY, POCSP_REQUEST_ENTRY structure pointer [Security], _OCSP_REQUEST_ENTRY, security.ocsp_request_entry, wincrypt/OCSP_REQUEST_ENTRY, wincrypt/POCSP_REQUEST_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Wincrypt.h
api_name:
 - OCSP_REQUEST_ENTRY
product: Windows
targetos: Windows
req.typenames: OCSP_REQUEST_ENTRY, *POCSP_REQUEST_ENTRY
req.redist: 
---

# _OCSP_REQUEST_ENTRY structure


## -description


The <b>OCSP_REQUEST_ENTRY</b> structure contains information about a single certificate in an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request. This structure populates the <a href="https://msdn.microsoft.com/ec939c3b-f155-45f2-b507-6c2e6069a868">OCSP_REQUEST_INFO</a> <b>rgRequestEntry</b> member.


## -struct-fields




### -field CertId

An <a href="https://msdn.microsoft.com/58717990-a7f7-4b41-aceb-cbce55411396">OCSP_CERT_ID</a> structure that specifies the target certificate.


### -field cExtension

The number of elements in the <b>rgExtension</b> array.


### -field rgExtension

An array of pointers to <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each of which contains information about the <b>CertId</b> certificate. 


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/58717990-a7f7-4b41-aceb-cbce55411396">OCSP_CERT_ID</a>



<a href="https://msdn.microsoft.com/ec939c3b-f155-45f2-b507-6c2e6069a868">OCSP_REQUEST_INFO</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560  Online Certificate Status Protocol</a>
 

 

