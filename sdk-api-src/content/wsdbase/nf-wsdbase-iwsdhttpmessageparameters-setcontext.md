---
UID: NF:wsdbase.IWSDHttpMessageParameters.SetContext
title: IWSDHttpMessageParameters::SetContext (wsdbase.h)
description: Sets the private transmission context for the current transaction.
helpviewer_keywords: ["IWSDHttpMessageParameters interface","SetContext method","IWSDHttpMessageParameters.SetContext","IWSDHttpMessageParameters::SetContext","SetContext","SetContext method","SetContext method","IWSDHttpMessageParameters interface","ncd.iwsdhttpmessageparameters_setcontext","wsdbase/IWSDHttpMessageParameters::SetContext"]
old-location: ncd\iwsdhttpmessageparameters_setcontext.htm
tech.root: ncd
ms.assetid: 8e1bbfbe-b7a7-4235-bb2d-8ee0ef301871
ms.date: 12/05/2018
ms.keywords: IWSDHttpMessageParameters interface,SetContext method, IWSDHttpMessageParameters.SetContext, IWSDHttpMessageParameters::SetContext, SetContext, SetContext method, SetContext method,IWSDHttpMessageParameters interface, ncd.iwsdhttpmessageparameters_setcontext, wsdbase/IWSDHttpMessageParameters::SetContext
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
 - IWSDHttpMessageParameters::SetContext
 - wsdbase/IWSDHttpMessageParameters::SetContext
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
 - IWSDHttpMessageParameters.SetContext
---

# IWSDHttpMessageParameters::SetContext


## -description

Sets the private transmission context for the current transaction.

## -parameters

### -param pContext [in]

Pointer to the desired private transmission context for the current transaction.

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
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>