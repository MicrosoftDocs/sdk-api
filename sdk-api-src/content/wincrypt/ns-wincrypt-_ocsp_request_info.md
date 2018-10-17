---
UID: NS:wincrypt._OCSP_REQUEST_INFO
title: "_OCSP_REQUEST_INFO"
author: windows-sdk-content
description: Contains information for an online certificate status protocol (OCSP) request as specified by RFC 2560.
old-location: security\ocsp_request_info.htm
tech.root: seccrypto
ms.assetid: ec939c3b-f155-45f2-b507-6c2e6069a868
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: "*POCSP_REQUEST_INFO, OCSP_REQUEST_INFO, OCSP_REQUEST_INFO structure [Security], OCSP_REQUEST_V1, POCSP_REQUEST_INFO, POCSP_REQUEST_INFO structure pointer [Security], _OCSP_REQUEST_INFO, security.ocsp_request_info, wincrypt/OCSP_REQUEST_INFO, wincrypt/POCSP_REQUEST_INFO"
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
 - OCSP_REQUEST_INFO
product: Windows
targetos: Windows
req.typenames: OCSP_REQUEST_INFO, *POCSP_REQUEST_INFO
req.redist: 
---

# _OCSP_REQUEST_INFO structure


## -description


The <b>OCSP_REQUEST_INFO</b> structure contains information for an  <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request as specified by <a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560</a>. The RFC specifies that a single request can contain a sequence of certificates for which statuses are required. The  <b>rgRequestEntry</b> member of this structure contains an <a href="https://msdn.microsoft.com/61d5cbc9-22de-4768-b610-138bcd3c9cce">OCSP_REQUEST_ENTRY</a> structure for each certificate in a sequence.


## -struct-fields




### -field dwVersion

A value that indicates the protocol version of the OCSP request.



#### OCSP_REQUEST_V1 (0)


### -field pRequestorName

A pointer to a <a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a> structure that contains the name bound to the certificate <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> of the requester.


### -field cRequestEntry

The number of elements in the <b>rgRequestEntry</b> array.


### -field rgRequestEntry

An array of pointers to <a href="https://msdn.microsoft.com/61d5cbc9-22de-4768-b610-138bcd3c9cce">OCSP_REQUEST_ENTRY</a> structures.


### -field cExtension

The number of elements in the <b>rgExtension</b> array.


### -field rgExtension

An array of pointers to <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each of which contains information about the request.


## -see-also




<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a>



<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/61d5cbc9-22de-4768-b610-138bcd3c9cce">OCSP_REQUEST_ENTRY</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560 Online Certificate Status Protocol</a>
 

 

