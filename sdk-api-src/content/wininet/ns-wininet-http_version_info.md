---
UID: NS:wininet.HTTP_VERSION_INFO
title: HTTP_VERSION_INFO (wininet.h)
description: Contains the global HTTP version.
helpviewer_keywords: ["*LPHTTP_VERSION_INFO","HTTP_VERSION_INFO","HTTP_VERSION_INFO structure [WinINet]","LPHTTP_VERSION_INFO","LPHTTP_VERSION_INFO structure pointer [WinINet]","_inet_http_version_info_structure","wininet.http_version_info","wininet/HTTP_VERSION_INFO","wininet/LPHTTP_VERSION_INFO"]
old-location: wininet\http_version_info.htm
tech.root: wininet
ms.assetid: 446da4aa-08be-4b2c-a436-dc8fa923a3a8
ms.date: 12/05/2018
ms.keywords: '*LPHTTP_VERSION_INFO, HTTP_VERSION_INFO, HTTP_VERSION_INFO structure [WinINet], LPHTTP_VERSION_INFO, LPHTTP_VERSION_INFO structure pointer [WinINet], _inet_http_version_info_structure, wininet.http_version_info, wininet/HTTP_VERSION_INFO, wininet/LPHTTP_VERSION_INFO'
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
req.typenames: HTTP_VERSION_INFO, *LPHTTP_VERSION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPHTTP_VERSION_INFO
 - wininet/LPHTTP_VERSION_INFO
 - HTTP_VERSION_INFO
 - wininet/HTTP_VERSION_INFO
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
 - HTTP_VERSION_INFO
---

# HTTP_VERSION_INFO structure


## -description

Contains the global HTTP version.

## -struct-fields

### -field dwMajorVersion

The major version number. Must be 1.

### -field dwMinorVersion

The minor version number. Can be either 1 or zero.

## -remarks

On Windows 7, Windows Server 2008 R2, and later, the value in the <b>HTTP_VERSION_INFO</b> structure is overridden by Internet Explorer settings.  <b>EnableHttp1_1</b> is a registry value under <b>HKLM\Software\Microsoft\InternetExplorer\AdvacnedOptions\HTTP\GENABLE</b> controlled by Internet Options set in Internet Explorer for the system.  The <b>EnableHttp1_1</b> value defaults to 1. The <b>HTTP_VERSION_INFO</b> structure is  ignored for any HTTP version less than 1.1 if <b>EnableHttp1_1</b> is set to 1.


<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>

