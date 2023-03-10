---
UID: NF:webservices.WsResetError
title: WsResetError function (webservices.h)
description: Releases the content of the error object parameter but does not release the resource allocated to the error object parameter.
helpviewer_keywords: ["WsResetError","WsResetError function [Web Services for Windows]","webservices/WsResetError","wsw.wsreseterror"]
old-location: wsw\wsreseterror.htm
tech.root: wsw
ms.assetid: a01a65f1-3eca-452c-a10d-dc9c6c3db124
ms.date: 12/05/2018
ms.keywords: WsResetError, WsResetError function [Web Services for Windows], webservices/WsResetError, wsw.wsreseterror
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
 - WsResetError
 - webservices/WsResetError
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
 - WsResetError
---

# WsResetError function


## -description

Releases the content of the <i>error</i> object parameter but does not release the resource allocated to the <i>error</i> object parameter. 
            <div class="alert"><b>Note</b>  The "reset" effect of this function returns the <i>error</i> object to the state set at instantiation. The object is not released consequently is available for reuse.
            </div>
<div> </div>

## -parameters

### -param error [in]

This parameter is a   pointer to the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object to reset.

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
</table>

## -remarks

String data added to the error object using the <a href="/windows/desktop/api/webservices/nf-webservices-wsadderrorstring">WsAddErrorString</a> function are released.
            

Properties that have been set using the  <a href="/windows/desktop/api/webservices/nf-webservices-wsseterrorproperty">WsSetErrorProperty</a> function are released.