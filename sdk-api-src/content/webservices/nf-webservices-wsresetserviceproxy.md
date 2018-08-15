---
UID: NF:webservices.WsResetServiceProxy
title: WsResetServiceProxy function
author: windows-sdk-content
description: Resets service proxy.
old-location: wsw\wsresetserviceproxy.htm
old-project: wsw
ms.assetid: 6a99c958-92f9-4487-8768-3265dab7f0ea
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsResetServiceProxy, WsResetServiceProxy function [Web Services for Windows], webservices/WsResetServiceProxy, wsw.wsresetserviceproxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsResetServiceProxy
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsResetServiceProxy function


## -description


Resets service proxy.

WsResetServiceProxy provides a convenient way to reuse the service proxy. 
                Once the proxy is <a href="https://msdn.microsoft.com/82156e64-ae95-4a4a-aaad-e3dd69832c97">closed</a>,
                the application can call WsResetServiceProxy to reuse it.
            

Reusing the service proxy is helpful in scenarios where an application connects 
                to the same service time and time again. The cost of initialization is only paid 
                once during the initial creation of the service proxy.
            


## -parameters




### -param serviceProxy [in]

The service proxy.


### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The serviceProxy was in an inappropriate state.

</td>
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
</table>
 



