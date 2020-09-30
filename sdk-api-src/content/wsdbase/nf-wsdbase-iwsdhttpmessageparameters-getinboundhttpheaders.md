---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetInboundHttpHeaders
title: IWSDHttpMessageParameters::GetInboundHttpHeaders (wsdbase.h)
description: Retrieves the current HTTP headers used for inbound SOAP-over-HTTP transmissions.
helpviewer_keywords: ["GetInboundHttpHeaders","GetInboundHttpHeaders method","GetInboundHttpHeaders method","IWSDHttpMessageParameters interface","IWSDHttpMessageParameters interface","GetInboundHttpHeaders method","IWSDHttpMessageParameters.GetInboundHttpHeaders","IWSDHttpMessageParameters::GetInboundHttpHeaders","ncd.iwsdhttpmessageparameters_getinboundhttpheaders","wsdbase/IWSDHttpMessageParameters::GetInboundHttpHeaders"]
old-location: ncd\iwsdhttpmessageparameters_getinboundhttpheaders.htm
tech.root: ncd
ms.assetid: 99b30444-1059-45c3-ac72-a0f98d722365
ms.date: 12/05/2018
ms.keywords: GetInboundHttpHeaders, GetInboundHttpHeaders method, GetInboundHttpHeaders method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetInboundHttpHeaders method, IWSDHttpMessageParameters.GetInboundHttpHeaders, IWSDHttpMessageParameters::GetInboundHttpHeaders, ncd.iwsdhttpmessageparameters_getinboundhttpheaders, wsdbase/IWSDHttpMessageParameters::GetInboundHttpHeaders
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
 - IWSDHttpMessageParameters::GetInboundHttpHeaders
 - wsdbase/IWSDHttpMessageParameters::GetInboundHttpHeaders
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
 - IWSDHttpMessageParameters.GetInboundHttpHeaders
---

# IWSDHttpMessageParameters::GetInboundHttpHeaders


## -description

Retrieves the current HTTP headers used for inbound SOAP-over-HTTP transmissions.

## -parameters

### -param ppszHeaders [out]

Pointer used to receive the current HTTP headers in use. Do not deallocate this pointer.

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
<i>ppszHeaders</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There are no headers available.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>