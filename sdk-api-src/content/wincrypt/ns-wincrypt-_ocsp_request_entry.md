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
 

 

