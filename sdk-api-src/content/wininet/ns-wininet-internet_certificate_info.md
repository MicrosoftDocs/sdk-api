---
UID: NS:wininet.INTERNET_CERTIFICATE_INFO
title: INTERNET_CERTIFICATE_INFO
author: windows-sdk-content
description: Contains certificate information returned from the server. This structure is used by the InternetQueryOption function.
old-location: wininet\internet_certificate_info.htm
old-project: WinInet
ms.assetid: 2262a3cf-f325-470a-a7cd-9bcafc5aadc4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPINTERNET_CERTIFICATE_INFO, INTERNET_CERTIFICATE_INFO, INTERNET_CERTIFICATE_INFO structure [WinINet], LPINTERNET_CERTIFICATE_INFO, LPINTERNET_CERTIFICATE_INFO structure pointer [WinINet], _inet_internet_certificate_info_structure, wininet.internet_certificate_info, wininet/ LPINTERNET_CERTIFICATE_INFO, wininet/INTERNET_CERTIFICATE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: INTERNET_CERTIFICATE_INFO, *LPINTERNET_CERTIFICATE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_CERTIFICATE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

