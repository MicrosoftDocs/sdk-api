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
 

 

