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

# WsDecodeUrl function


## -description


Evaluates the components of an URL to determine its "scheme". A <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> value is encapsulated in a <a href="https://msdn.microsoft.com/efc67b64-cedf-4cd9-83b3-047f6c38c6ea">WS_URL</a> structure and a reference to the structure is returned via output parameter. 
                If the scheme is not recognized, the function returns WS_E_INVALID_FORMAT.    
                Only scheme types identified in  <b>WS_URL_SCHEME_TYPE</b> are supported.
            


## -parameters




### -param url [in]

A pointer to a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a>  representation of the URL to evaluate.
                


### -param flags [in]

Determines the URL scheme evaluation method.  See <a href="https://msdn.microsoft.com/b74c22fd-35b1-4d7b-974d-8ff7fff07813">WS_URL_FLAGS</a>.
                


### -param heap [in]

A pointer to a <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> in which to allocate the returned URL reference.
                


### -param outUrl


                    Reference to the <a href="https://msdn.microsoft.com/efc67b64-cedf-4cd9-83b3-047f6c38c6ea">WS_URL</a> structure that encapsulates the <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> value.
                


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

                    The input URL was not in the correct format, or the scheme was not recognized.
                

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




                The grammar parsed for the schemes "http", "https", "net.tcp" and "soap.udp" can be found at http://www.ietf.org/rfc/rfc3986.txt.  For these schemes:
                    <ul>
<li>A non-empty hostname is required.
                      </li>
<li>For the IP-literal production all the characters demarcated by "[" and "]" are returned.  They are not enforced to follow the IPv6Address production.
                    </li>
<li>The userinfo part of authority (for example, userinfo@hostname:port) is not supported.
                    </li>
</ul>



                If no port is specified the default port for that scheme is returned.
            

If no port is specified for the soap.udp scheme 0xFFFFFFFF is returned as the default.
            



