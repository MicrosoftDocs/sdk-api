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

# INTERNET_CERTIFICATE_INFO structure


## -description


Contains certificate information returned from the server. This structure is used by the 
<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> function.


## -struct-fields




### -field ftExpiry


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date the certificate expires.


### -field ftStart


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date the certificate becomes valid.


### -field lpszSubjectInfo

Pointer to a buffer that contains the name of the organization, site, and server for which the certificate was issued. The application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the resources allocated for this parameter.


### -field lpszIssuerInfo

Pointer to a buffer that contains the name of the organization, site, and server that issued the certificate. The application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the resources allocated for this parameter.


### -field lpszProtocolName

Pointer to a buffer that contains the name of the protocol used to provide the secure connection. The application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the resources allocated for this parameter.


### -field lpszSignatureAlgName

Pointer to a buffer that contains the name of the algorithm used for signing the certificate. The application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the resources allocated for this parameter.


### -field lpszEncryptionAlgName

Pointer to a buffer that contains the name of the algorithm used for doing encryption over the secure channel (SSL/PCT) connection. The application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the resources allocated for this parameter.


### -field dwKeySize

Size, in <b>TCHAR</b>s, of the key.


## -remarks



Despite what the header indicates, the implementation of <b>INTERNET_CERTIFICATE_INFO</b> is not Unicode-aware.  All of the string members are filled as ANSI strings regardless of whether Unicode is enabled.  Consequently, when reading these values, the caller must cast them to LPSTR if Unicode is enabled.

Applications requesting this information must free pointers that are allocated and placed in the returned structure.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>
 

 

