---
UID: NF:wsdbase.IWSDHttpMessageParameters.SetOutboundHttpHeaders
title: IWSDHttpMessageParameters::SetOutboundHttpHeaders (wsdbase.h)
description: Sets the HTTP headers used for outbound SOAP-over-HTTP transmissions.
helpviewer_keywords: ["IWSDHttpMessageParameters interface","SetOutboundHttpHeaders method","IWSDHttpMessageParameters.SetOutboundHttpHeaders","IWSDHttpMessageParameters::SetOutboundHttpHeaders","SetOutboundHttpHeaders","SetOutboundHttpHeaders method","SetOutboundHttpHeaders method","IWSDHttpMessageParameters interface","ncd.iwsdhttpmessageparameters_setoutboundhttpheaders","wsdbase/IWSDHttpMessageParameters::SetOutboundHttpHeaders"]
old-location: ncd\iwsdhttpmessageparameters_setoutboundhttpheaders.htm
tech.root: ncd
ms.assetid: f54f86dc-4b25-4faa-8a37-b241e9ba8c6c
ms.date: 12/05/2018
ms.keywords: IWSDHttpMessageParameters interface,SetOutboundHttpHeaders method, IWSDHttpMessageParameters.SetOutboundHttpHeaders, IWSDHttpMessageParameters::SetOutboundHttpHeaders, SetOutboundHttpHeaders, SetOutboundHttpHeaders method, SetOutboundHttpHeaders method,IWSDHttpMessageParameters interface, ncd.iwsdhttpmessageparameters_setoutboundhttpheaders, wsdbase/IWSDHttpMessageParameters::SetOutboundHttpHeaders
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
 - IWSDHttpMessageParameters::SetOutboundHttpHeaders
 - wsdbase/IWSDHttpMessageParameters::SetOutboundHttpHeaders
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
 - IWSDHttpMessageParameters.SetOutboundHttpHeaders
---

# IWSDHttpMessageParameters::SetOutboundHttpHeaders


## -description

Sets the HTTP headers used for outbound SOAP-over-HTTP transmissions.

## -parameters

### -param pszHeaders [in]

The HTTP headers to be set.

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
The length in characters of <i>pszHeaders</i> exceeds WSD_MAX_TEXT_LENGTH (8192). 

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

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>