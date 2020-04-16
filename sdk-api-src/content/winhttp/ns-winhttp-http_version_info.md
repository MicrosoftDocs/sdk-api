---
UID: NS:winhttp.__unnamed_struct_1
title: HTTP_VERSION_INFO (winhttp.h)
description: The HTTP_VERSION_INFO structure contains the global HTTP version.
old-location: http\http_version_info.htm
tech.root: WinHttp
ms.assetid: 2d794a99-7bd2-43ad-b826-f160bf78ccac
ms.date: 12/05/2018
ms.keywords: '*LPHTTP_VERSION_INFO, HTTP_VERSION_INFO, HTTP_VERSION_INFO structure [HTTP], http.http_version_info, winhttp/HTTP_VERSION_INFO, winhttp_http_version_info_structure'
f1_keywords:
- winhttp/HTTP_VERSION_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winhttp.h
api_name:
- HTTP_VERSION_INFO
targetos: Windows
req.typenames: HTTP_VERSION_INFO, *LPHTTP_VERSION_INFO
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
---

## -description

The <b>HTTP_VERSION_INFO</b> structure contains the global HTTP version.

## -struct-fields

### -field dwMajorVersion

Major version number. Must be 1. 

### -field dwMinorVersion

Minor version number. Can be either 1 or 0. 

## -remarks

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>