---
UID: NS:wininet.INTERNET_CERTIFICATE_INFO
title: INTERNET_CERTIFICATE_INFO (wininet.h)
description: Contains certificate information returned from the server. This structure is used by the InternetQueryOption function.
helpviewer_keywords: ["*LPINTERNET_CERTIFICATE_INFO","INTERNET_CERTIFICATE_INFO","INTERNET_CERTIFICATE_INFO structure [WinINet]","LPINTERNET_CERTIFICATE_INFO","LPINTERNET_CERTIFICATE_INFO structure pointer [WinINet]","_inet_internet_certificate_info_structure","wininet.internet_certificate_info","wininet/ LPINTERNET_CERTIFICATE_INFO","wininet/INTERNET_CERTIFICATE_INFO"]
old-location: wininet\internet_certificate_info.htm
tech.root: wininet
ms.assetid: 2262a3cf-f325-470a-a7cd-9bcafc5aadc4
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_CERTIFICATE_INFO, INTERNET_CERTIFICATE_INFO, INTERNET_CERTIFICATE_INFO structure [WinINet], LPINTERNET_CERTIFICATE_INFO, LPINTERNET_CERTIFICATE_INFO structure pointer [WinINet], _inet_internet_certificate_info_structure, wininet.internet_certificate_info, wininet/ LPINTERNET_CERTIFICATE_INFO, wininet/INTERNET_CERTIFICATE_INFO'
req.header: wininet.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_CERTIFICATE_INFO, *LPINTERNET_CERTIFICATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_CERTIFICATE_INFO
 - wininet/LPINTERNET_CERTIFICATE_INFO
 - INTERNET_CERTIFICATE_INFO
 - wininet/INTERNET_CERTIFICATE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_CERTIFICATE_INFO
---

# INTERNET_CERTIFICATE_INFO structure


## -description

Contains certificate information returned from the server. This structure is used by the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a> function.

## -struct-fields

### -field ftExpiry

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date the certificate expires.

### -field ftStart

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date the certificate becomes valid.

### -field lpszSubjectInfo

Pointer to a buffer that contains the name of the organization, site, and server for which the certificate was issued. The application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the resources allocated for this parameter.

### -field lpszIssuerInfo

Pointer to a buffer that contains the name of the organization, site, and server that issued the certificate. The application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the resources allocated for this parameter.

### -field lpszProtocolName

Pointer to a buffer that contains the name of the protocol used to provide the secure connection. The application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the resources allocated for this parameter.

### -field lpszSignatureAlgName

Pointer to a buffer that contains the name of the algorithm used for signing the certificate. The application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the resources allocated for this parameter.

### -field lpszEncryptionAlgName

Pointer to a buffer that contains the name of the algorithm used for doing encryption over the secure channel (SSL/PCT) connection. The application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the resources allocated for this parameter.

### -field dwKeySize

Size, in <b>TCHAR</b>s, of the key.

## -remarks

Despite what the header indicates, the implementation of <b>INTERNET_CERTIFICATE_INFO</b> is not Unicode-aware.  All of the string members are filled as ANSI strings regardless of whether Unicode is enabled.  Consequently, when reading these values, the caller must cast them to LPSTR if Unicode is enabled.

Applications requesting this information must free pointers that are allocated and placed in the returned structure.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>

