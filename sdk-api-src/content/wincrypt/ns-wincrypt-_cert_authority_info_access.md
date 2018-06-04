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

# _CERT_AUTHORITY_INFO_ACCESS structure


## -description


The <b>CERT_AUTHORITY_INFO_ACCESS</b> structure represents authority information access and subject information access certificate extensions and specifies how to access additional information and services for the subject or the issuer of a certificate.


## -struct-fields




### -field cAccDescr

The number of elements in the <b>rgAccDescr</b> array.


### -field rgAccDescr

An array of pointers to 
<a href="https://msdn.microsoft.com/5e1e5b04-92af-45b1-acfd-17852c245d89">CERT_ACCESS_DESCRIPTION</a> structures that describes the format and location of additional information about the certificate. Each <b>CERT_ACCESS_DESCRIPTION</b> structure has as its members a <b>pszAccessMethod</b> string that indicates an access method and a 
<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a> structure that indicates the location of the additional information.


## -remarks




				The type of information represented by this structure depends on the access methods specified by the <a href="https://msdn.microsoft.com/5e1e5b04-92af-45b1-acfd-17852c245d89">CERT_ACCESS_DESCRIPTION</a> structures in the <i>rgAccDescr</i> array. For more information about access methods, the authority information access extension, and the subject information access extension, see <a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>.

The <a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> function creates an instance of this structure when decoding a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member and the <b>pszObjId</b> member of the <b>CERT_EXTENSION</b> structure is set to szOID_AUTHORITY_INFO_ACCESS or szOID_SUBJECT_INFO_ACCESS.

An instance of this structure can be used as input to the <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> function to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e1e5b04-92af-45b1-acfd-17852c245d89">CERT_ACCESS_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>
 

 

