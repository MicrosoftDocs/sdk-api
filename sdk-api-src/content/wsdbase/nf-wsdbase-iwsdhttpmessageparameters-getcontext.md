---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetContext
title: IWSDHttpMessageParameters::GetContext (wsdbase.h)
description: Retrieves the private transmission context for the current transaction.
helpviewer_keywords: ["GetContext","GetContext method","GetContext method","IWSDHttpMessageParameters interface","IWSDHttpMessageParameters interface","GetContext method","IWSDHttpMessageParameters.GetContext","IWSDHttpMessageParameters::GetContext","ncd.iwsdhttpmessageparameters_getcontext","wsdbase/IWSDHttpMessageParameters::GetContext"]
old-location: ncd\iwsdhttpmessageparameters_getcontext.htm
tech.root: ncd
ms.assetid: af93f97f-a3de-4b5c-92c5-2d4ab91e7985
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method, GetContext method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetContext method, IWSDHttpMessageParameters.GetContext, IWSDHttpMessageParameters::GetContext, ncd.iwsdhttpmessageparameters_getcontext, wsdbase/IWSDHttpMessageParameters::GetContext
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDHttpMessageParameters::GetContext
 - wsdbase/IWSDHttpMessageParameters::GetContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpMessageParameters.GetContext
---

# IWSDHttpMessageParameters::GetContext


## -description

Retrieves the private transmission context for the current transaction.

## -parameters

### -param ppContext [out]

Pointer to the pointer used to retrieve the desired private transmission context for the current transaction.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<i>ppContext</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Could not retrieve the context.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>