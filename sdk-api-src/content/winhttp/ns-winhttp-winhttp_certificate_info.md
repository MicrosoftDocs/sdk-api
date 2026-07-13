---
UID: NS:winhttp._WINHTTP_CERTIFICATE_INFO
title: WINHTTP_CERTIFICATE_INFO (winhttp.h)
description: The WINHTTP_CERTIFICATE_INFO structure contains certificate information returned from the server. This structure is used by the WinHttpQueryOption function.
helpviewer_keywords: ["WINHTTP_CERTIFICATE_INFO","WINHTTP_CERTIFICATE_INFO structure [HTTP]","http.internet_certificate_info","winhttp/WINHTTP_CERTIFICATE_INFO","winhttp_internet_certificate_info_structure"]
old-location: http\internet_certificate_info.htm
tech.root: http
ms.assetid: 72b0094b-ac9d-499f-8a75-6728be2826ea
ms.date: 12/05/2018
ms.keywords: WINHTTP_CERTIFICATE_INFO, WINHTTP_CERTIFICATE_INFO structure [HTTP], http.internet_certificate_info, winhttp/WINHTTP_CERTIFICATE_INFO, winhttp_internet_certificate_info_structure
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
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
req.typenames: WINHTTP_CERTIFICATE_INFO
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WINHTTP_CERTIFICATE_INFO
 - winhttp/WINHTTP_CERTIFICATE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_CERTIFICATE_INFO
---

## -description

The <b>WINHTTP_CERTIFICATE_INFO</b> structure contains certificate information returned from the server. This structure is used by the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> function.

## -struct-fields

### -field ftExpiry

A 
						<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date the certificate expires.

### -field ftStart

A 
						<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date the certificate becomes valid.

### -field lpszSubjectInfo

A pointer to a buffer that contains the name of the organization, site, and server for which the certificate was issued.

### -field lpszIssuerInfo

A pointer to a buffer that contains the name of the organization, site, and server that issued the certificate.

### -field lpszProtocolName

A pointer to a buffer that contains the name of the protocol used to provide the secure connection. This member is not current used.

### -field lpszSignatureAlgName

A pointer to a buffer that contains the name of the algorithm used to sign the certificate. This member is not current used.

### -field lpszEncryptionAlgName

A pointer to a buffer that contains the name of the algorithm used to perform encryption over the secure channel (SSL/TLS) connection. This member is not current used.

### -field dwKeySize

The size, in bytes, of the key.

## -remarks

The <b>WINHTTP_CERTIFICATE_INFO</b> structure contains information on the certificate returned by the server when the connection uses SSL/TLS. The <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> function returns the <b>WINHTTP_CERTIFICATE_INFO</b> structure when the <i>dwOption</i> parameter passed to the <b>WinHttpQueryOption</b> function is set to <b>WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT</b>. For more information, see <a href="/windows/desktop/WinHttp/option-flags">Option Flags</a>.

The <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> function does not set  the <b>lpszProtocolName</b>, <b>lpszSignatureAlgName</b>, and <b>lpszEncryptionAlgName</b> members of the <b>WINHTTP_CERTIFICATE_INFO</b> structure, so these member are always returned as <b>NULL</b>.

Once the application no longer needs the returned <b>WINHTTP_CERTIFICATE_INFO</b> structure, the  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function should be called to free any pointers returned in the structure. The structure members containing pointers that are not NULL and need to be freed are <b>lpszSubjectInfo</b> and <b>lpszIssuerInfo</b>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the <a href="/windows/desktop/WinHttp/winhttp-start-page">Windows HTTP Services</a> start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/option-flags">Option Flags</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP
		  Versions</a>


<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a>