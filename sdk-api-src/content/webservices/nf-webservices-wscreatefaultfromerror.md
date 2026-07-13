---
UID: NF:webservices.WsCreateFaultFromError
title: WsCreateFaultFromError function (webservices.h)
description: Constructs a WS_FAULT from a specified error object.
helpviewer_keywords: ["WsCreateFaultFromError","WsCreateFaultFromError function [Web Services for Windows]","webservices/WsCreateFaultFromError","wsw.wscreatefaultfromerror"]
old-location: wsw\wscreatefaultfromerror.htm
tech.root: wsw
ms.assetid: 193854d7-3b7f-4f2b-b068-33b9c4d91e57
ms.date: 12/05/2018
ms.keywords: WsCreateFaultFromError, WsCreateFaultFromError function [Web Services for Windows], webservices/WsCreateFaultFromError, wsw.wscreatefaultfromerror
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
 - WsCreateFaultFromError
 - webservices/WsCreateFaultFromError
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
 - WsCreateFaultFromError
---

# WsCreateFaultFromError function


## -description

Constructs a <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a>  from a specified error object.

## -parameters

### -param error [in]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure representing the error object from which to construct the fault.

### -param faultErrorCode [in]

The HRESULT error code returned from the function that failed.
                    The HRESULT value cannot be a success code.
                

This error code is never included in the fault directly, but is used as a fallback mechanism for creating a fault string if the error object does not contain any error strings.

### -param faultDisclosure [in]

<a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_disclosure">WS_FAULT_DISCLOSURE</a> enumeration that controls
                    what information is copied from
                    the error object to the fault object.

### -param heap [in]

Pointer to a <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> structure representing the <a href="/windows/desktop/wsw/heap">heap</a> from which to allocate memory for the returned fault object.

### -param fault [out]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a> structure representing the returned fault object.  The fields of the fault object are good until
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeheap">WsFreeHeap</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsresetheap">WsResetHeap</a> is called to release the specified heap resources.

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

If the error object contains a fault (that is, the WS_FAULT_ERROR_PROPERTY_FAULT value of <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_error_property_id">WS_FAULT_ERROR_PROPERTY_ID</a>   is non-<b>NULL</b>), then that fault is selected to construct the returned fault.

If the error object does not contain a fault (WS_FAULT_ERROR_PROPERTY_FAULT is <b>NULL</b>),  a generic fault with a generic fault code (and no reason text) is selected to construct the returned fault. 

If the selected fault does not include any reason text,  the fault reason
                text is constructed according to the value of <i>disclosure</i> parameter:
                <ul>
<li>WS_FULL_FAULT_DISCLOSURE
                    All the error strings present in the error object are appended together
                    to form the reason text.  If there are no strings, the string associated
                    with the <i>errorCode</i> parameter is used.
                    </li>
<li>WS_MINIMAL_FAULT_DISCLOSURE
                    A generic error string is used.
                </li>
</ul>


By default, the
                language of any language-dependent information in the error object is  the current 
                user default UI language. However, you can change the language by setting 
                the WS_ERROR_PROPERTY_LANGID property. See the <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ID</a> enumeration.