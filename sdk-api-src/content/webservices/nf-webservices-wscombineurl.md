---
UID: NF:webservices.WsCombineUrl
title: WsCombineUrl function (webservices.h)
description: Produces an absolute URL from a specified URL reference (absolute or relative URL) and a specified absolute base URL.
helpviewer_keywords: ["WsCombineUrl","WsCombineUrl function [Web Services for Windows]","webservices/WsCombineUrl","wsw.wscombineurl"]
old-location: wsw\wscombineurl.htm
tech.root: wsw
ms.assetid: 6cff906a-adb7-4453-8d44-6a5bf44a681b
ms.date: 12/05/2018
ms.keywords: WsCombineUrl, WsCombineUrl function [Web Services for Windows], webservices/WsCombineUrl, wsw.wscombineurl
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCombineUrl
 - webservices/WsCombineUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCombineUrl
---

# WsCombineUrl function


## -description

Produces an absolute URL from a specified URL reference (absolute or relative URL) and a specified absolute base URL.

## -parameters

### -param baseUrl [in]

Pointer to a <a href="/windows/desktop/wsw/ws-listener">WS_STRING</a> structure containing an absolute URL in encoded format.

### -param referenceUrl [in]

Pointer to a <a href="/windows/desktop/wsw/ws-listener">WS_STRING</a> structure  containing an absolute or relative URL in encoded format.

### -param flags [in]

Controls the  format of the resulting URL.  For more information, see <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type">WS_URL_FLAGS</a>.

### -param heap [in]

Pointer to the <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> object from which the memory for the resulting URL is allocated.

### -param resultUrl [out]

Pointer to a <a href="/windows/desktop/wsw/ws-listener">WS_STRING</a> structure that receives the resulting URL.
                This is an absolute URL in encoded format.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The base URL or reference URL was not in the correct format, or 
                    had a scheme that was not recognized.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

If the reference URL is absolute, it is returned unchanged, if the specified flags permit.
            If the reference URL is relative, it is combined with the base URL before being returned.
            

Only the schemes listed in <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> are supported.