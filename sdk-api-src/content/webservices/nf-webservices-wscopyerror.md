---
UID: NF:webservices.WsCopyError
title: WsCopyError function (webservices.h)
description: Copies an error object from a specified source to a specified destination.
helpviewer_keywords: ["WsCopyError","WsCopyError function [Web Services for Windows]","webservices/WsCopyError","wsw.wscopyerror"]
old-location: wsw\wscopyerror.htm
tech.root: wsw
ms.assetid: 02b44bd4-b7ce-4be5-bd59-340c006a1e43
ms.date: 12/05/2018
ms.keywords: WsCopyError, WsCopyError function [Web Services for Windows], webservices/WsCopyError, wsw.wscopyerror
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
 - WsCopyError
 - webservices/WsCopyError
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
 - WsCopyError
---

# WsCopyError function


## -description

Copies an error object from a specified source  to a specified destination.

## -parameters

### -param source [in]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure representing the error object to copy.

### -param destination [in]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure that receives the copied error object.

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
One of the error objects is <b>NULL</b>.
                

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