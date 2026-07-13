---
UID: NF:wsdbase.WSDCreateHttpMessageParameters
title: WSDCreateHttpMessageParameters function (wsdbase.h)
description: Creates an IWSDHttpMessageParameters object.
helpviewer_keywords: ["WSDCreateHttpMessageParameters","WSDCreateHttpMessageParameters function","ncd.wsdcreatehttpmessageparameters","wsdbase/WSDCreateHttpMessageParameters"]
old-location: ncd\wsdcreatehttpmessageparameters.htm
tech.root: ncd
ms.assetid: 43797991-7a9c-42f8-bf64-655bde014487
ms.date: 12/05/2018
ms.keywords: WSDCreateHttpMessageParameters, WSDCreateHttpMessageParameters function, ncd.wsdcreatehttpmessageparameters, wsdbase/WSDCreateHttpMessageParameters
req.header: wsdbase.h
req.include-header: Wsdapi.h
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
req.lib: wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDCreateHttpMessageParameters
 - wsdbase/WSDCreateHttpMessageParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateHttpMessageParameters
---

# WSDCreateHttpMessageParameters function


## -description

Creates an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a> object.

## -parameters

### -param ppTxParams

Returns a reference to the initialized <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a> object. Cannot be <b>NULL</b>.

## -returns

Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppTxParams</i> is <b>NULL</b>.

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
</table>