---
UID: NF:webservices.WsResetServiceHost
title: WsResetServiceHost function (webservices.h)
description: Resets service host so that it can be opened again.
helpviewer_keywords: ["WsResetServiceHost","WsResetServiceHost function [Web Services for Windows]","webservices/WsResetServiceHost","wsw.wsresetservicehost"]
old-location: wsw\wsresetservicehost.htm
tech.root: wsw
ms.assetid: 99f57173-8d7e-41e6-bf1e-4e8177b740b7
ms.date: 12/05/2018
ms.keywords: WsResetServiceHost, WsResetServiceHost function [Web Services for Windows], webservices/WsResetServiceHost, wsw.wsresetservicehost
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WsResetServiceHost
 - webservices/WsResetServiceHost
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
 - WsResetServiceHost
---

# WsResetServiceHost function


## -description

Resets service host so that it can be opened again.
            

Rather the creating a new service host from scratch <b>WsResetServiceHost</b> 
                provides a convenient way to reuse service host. Specifically in a scenario 
                where a service host has to go through close and open on a regular basis, 
                this allows for an efficient way for reusing the same service host. It resets 
                the underlying channel and listeners for reuse.

## -parameters

### -param serviceHost [in]

The service host to reset.

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
The serviceHost was in an inappropriate state.

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

