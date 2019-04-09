---
UID: NF:webservices.WsEncodeUrl
title: WsEncodeUrl function (webservices.h)
author: windows-sdk-content
description: Encodes the specified WS_URL into a URL string given its component parts. Values are escaped as necessary, combined, and stored in the specified WS_HEAP, and the result is returned as a WS_STRING.
old-location: wsw\wsencodeurl.htm
tech.root: wsw
ms.assetid: 8253b062-072b-4d37-8b82-407df1bea6b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsEncodeUrl, WsEncodeUrl function [Web Services for Windows], webservices/WsEncodeUrl, wsw.wsencodeurl
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsEncodeUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsEncodeUrl function


## -description


Encodes the specified <a href="https://msdn.microsoft.com/efc67b64-cedf-4cd9-83b3-047f6c38c6ea">WS_URL</a> into a URL string given its component parts. Values are escaped as necessary,
                combined, and stored in the specified <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>, and the result is returned as a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a>.


## -parameters




### -param url [in]

A reference to the  <a href="https://msdn.microsoft.com/efc67b64-cedf-4cd9-83b3-047f6c38c6ea">WS_URL</a> to encode.
                


### -param flags [in]

The value of this parameter determines the URL scheme evaluation method.  See <a href="https://msdn.microsoft.com/b74c22fd-35b1-4d7b-974d-8ff7fff07813">WS_URL_FLAGS</a>.
                


### -param heap [in]

A pointer to a <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> in which to allocate URL.
                


### -param outUrl [out]

A pointer to the resulting URL string.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

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
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The URL data being encoded was not valid according to the URL syntax.                    
                

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



If a scheme is not recognized in the <i>url</i> parameter the function returns WS_E_INVALID_FORMAT.  
                Only scheme types identified in  <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> are supported.
            



