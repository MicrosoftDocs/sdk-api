---
UID: NF:webservices.WsCreateError
title: WsCreateError function (webservices.h)
description: Creates an error object that can passed to functions to record rich error information.
helpviewer_keywords: ["WsCreateError","WsCreateError function [Web Services for Windows]","webservices/WsCreateError","wsw.wscreateerror"]
old-location: wsw\wscreateerror.htm
tech.root: wsw
ms.assetid: 0ec858f7-12a5-43cf-94a7-3838ab6d76ae
ms.date: 12/05/2018
ms.keywords: WsCreateError, WsCreateError function [Web Services for Windows], webservices/WsCreateError, wsw.wscreateerror
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
 - WsCreateError
 - webservices/WsCreateError
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
 - WsCreateError
---

# WsCreateError function


## -description

Creates an error object that can passed to functions to record rich error information.

## -parameters

### -param properties

An array of  <a href="/windows/desktop/api/webservices/ns-webservices-ws_error_property">WS_ERROR_PROPERTY</a> structures containing optional error properties.

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param error

On success, a pointer that receives the address of the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure representing the created error object.

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
Insufficient memory to complete the operation.

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

When you no long need the error object, free it by calling  the <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeerror">WsFreeError</a> function.
            

By default, the
                language of any language-dependent information in the error object is  the current 
                user default UI language. However, you can change the language by setting 
                the WS_ERROR_PROPERTY_LANGID property. See the <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ID</a> enumeration.