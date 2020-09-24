---
UID: NS:winhttp._WINHTTP_CONNECTION_INFO
title: WINHTTP_CONNECTION_INFO (winhttp.h)
description: The WINHTTP_CONNECTION_INFO structure contains the source and destination IP address of the request that generated the response.
helpviewer_keywords: ["WINHTTP_CONNECTION_INFO","WINHTTP_CONNECTION_INFO structure [HTTP]","http.winhttp_connection_info","winhttp/WINHTTP_CONNECTION_INFO"]
old-location: http\winhttp_connection_info.htm
tech.root: http
ms.assetid: cb6e10f8-a480-41ac-b4d3-f09cfc663780
ms.date: 12/05/2018
ms.keywords: WINHTTP_CONNECTION_INFO, WINHTTP_CONNECTION_INFO structure [HTTP], http.winhttp_connection_info, winhttp/WINHTTP_CONNECTION_INFO
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WINHTTP_CONNECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_CONNECTION_INFO
 - winhttp/_WINHTTP_CONNECTION_INFO
 - PWINHTTP_CONNECTION_INFO
 - winhttp/PWINHTTP_CONNECTION_INFO
 - WINHTTP_CONNECTION_INFO
 - winhttp/WINHTTP_CONNECTION_INFO
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
 - WINHTTP_CONNECTION_INFO
---

## -description

The <b>WINHTTP_CONNECTION_INFO</b> structure contains the source and destination IP address of the request that generated the response.

## -struct-fields

### -field cbSize

The size, in bytes, of the <b>WINHTTP_CONNECTION_INFO</b> structure.

### -field LocalAddress

A <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure that contains the local IP address and port of the original request.

### -field RemoteAddress

A <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure that contains the remote IP address and port of the original request.

## -remarks

When <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> returns, the application can retrieve the source and destination IP address of the request that generated the response. The application calls <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> with the <b>WINHTTP_OPTION_CONNECTION_INFO</b> option, and provides the <b>WINHTTP_CONNECTION_INFO</b> structure in the <i>lpBuffer</i> parameter.

#### Examples

The following code example shows the call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a>. Winsock2.h must be included before Winhttp.h when using the <b>WINHTTP_OPTION_CONNECTION_INFO</b> option.

If the original request was redirected, the <b>WINHTTP_CONNECTION_INFO</b> structure contains the IP address and port of the request that resulted from the first non-30X response.

```cpp
WINHTTP_CONNECTION_INFO ConnInfo;
DWORD dwConnInfoSize = sizeof(WINHTTP_CONNECTION_INFO);

WinHttpQueryOption( hRequest,
                    WINHTTP_OPTION_CONNECTION_INFO,
                    &ConnInfo,
                    &dwConnInfoSize);

```