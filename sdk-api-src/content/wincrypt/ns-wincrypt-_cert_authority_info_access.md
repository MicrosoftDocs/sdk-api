---
UID: NS:wincrypt._CERT_AUTHORITY_INFO_ACCESS
title: "_CERT_AUTHORITY_INFO_ACCESS"
author: windows-sdk-content
description: Represents authority information access and subject information access certificate extensions and specifies how to access additional information and services for the subject or the issuer of a certificate.
old-location: security\cert_authority_info_access.htm
tech.root: seccrypto
ms.assetid: 5f4abb15-3057-4d20-a319-550cec45d1f1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCERT_AUTHORITY_INFO_ACCESS, *PCERT_SUBJECT_INFO_ACCESS, CERT_AUTHORITY_INFO_ACCESS, CERT_AUTHORITY_INFO_ACCESS structure [Security], CERT_SUBJECT_INFO_ACCESS, CERT_SUBJECT_INFO_ACCESS structure [Security], PCERT_AUTHORITY_INFO_ACCESS, PCERT_AUTHORITY_INFO_ACCESS structure pointer [Security], PCERT_SUBJECT_INFO_ACCESS, PCERT_SUBJECT_INFO_ACCESS structure pointer [Security], _CERT_AUTHORITY_INFO_ACCESS, _crypto2_cert_authority_info_access, security.cert_authority_info_access, wincrypt/CERT_AUTHORITY_INFO_ACCESS, wincrypt/CERT_SUBJECT_INFO_ACCESS, wincrypt/PCERT_AUTHORITY_INFO_ACCESS, wincrypt/PCERT_SUBJECT_INFO_ACCESS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CERT_AUTHORITY_INFO_ACCESS
product: Windows
targetos: Windows
req.typenames: CERT_AUTHORITY_INFO_ACCESS, *PCERT_AUTHORITY_INFO_ACCESS, CERT_SUBJECT_INFO_ACCESS, *PCERT_SUBJECT_INFO_ACCESS
req.redist: 
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
 

 

