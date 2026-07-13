---
UID: NS:wininet.INTERNET_VERSION_INFO
title: INTERNET_VERSION_INFO (wininet.h)
description: Contains the HTTP version number of the server. This structure is used when passing the INTERNET_OPTION_VERSION flag to the InternetQueryOption function.
helpviewer_keywords: ["*LPINTERNET_VERSION_INFO","INTERNET_VERSION_INFO","INTERNET_VERSION_INFO structure [WinINet]","LPINTERNET_VERSION_INFO","LPINTERNET_VERSION_INFO structure pointer [WinINet]","_inet_internet_verion_info_structure","wininet.internet_version_info","wininet/ LPINTERNET_VERSION_INFO","wininet/INTERNET_VERSION_INFO"]
old-location: wininet\internet_version_info.htm
tech.root: wininet
ms.assetid: 6d979829-2451-47fa-a95f-81f447c93567
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_VERSION_INFO, INTERNET_VERSION_INFO, INTERNET_VERSION_INFO structure [WinINet], LPINTERNET_VERSION_INFO, LPINTERNET_VERSION_INFO structure pointer [WinINet], _inet_internet_verion_info_structure, wininet.internet_version_info, wininet/ LPINTERNET_VERSION_INFO, wininet/INTERNET_VERSION_INFO'
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
req.typenames: INTERNET_VERSION_INFO, *LPINTERNET_VERSION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_VERSION_INFO
 - wininet/LPINTERNET_VERSION_INFO
 - INTERNET_VERSION_INFO
 - wininet/INTERNET_VERSION_INFO
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
 - INTERNET_VERSION_INFO
---

# INTERNET_VERSION_INFO structure


## -description

Contains the HTTP version number of the server. This structure is used when passing the INTERNET_OPTION_VERSION flag to the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a> function.

## -struct-fields

### -field dwMajorVersion

Major version number.

### -field dwMinorVersion

Minor version number.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>

