---
UID: NF:wsdbase.IWSDSignatureProperty.IsMessageSignatureTrusted
title: IWSDSignatureProperty::IsMessageSignatureTrusted (wsdbase.h)
description: Specifies if a message signature is trusted.
helpviewer_keywords: ["IWSDSignatureProperty interface","IsMessageSignatureTrusted method","IWSDSignatureProperty.IsMessageSignatureTrusted","IWSDSignatureProperty::IsMessageSignatureTrusted","IsMessageSignatureTrusted","IsMessageSignatureTrusted method","IsMessageSignatureTrusted method","IWSDSignatureProperty interface","ncd.iwsdsignatureproperty_ismessagesignaturetrusted","wsdbase/IWSDSignatureProperty::IsMessageSignatureTrusted"]
old-location: ncd\iwsdsignatureproperty_ismessagesignaturetrusted.htm
tech.root: ncd
ms.assetid: b71ddd44-4823-455c-aea7-ee2f63b423bb
ms.date: 12/05/2018
ms.keywords: IWSDSignatureProperty interface,IsMessageSignatureTrusted method, IWSDSignatureProperty.IsMessageSignatureTrusted, IWSDSignatureProperty::IsMessageSignatureTrusted, IsMessageSignatureTrusted, IsMessageSignatureTrusted method, IsMessageSignatureTrusted method,IWSDSignatureProperty interface, ncd.iwsdsignatureproperty_ismessagesignaturetrusted, wsdbase/IWSDSignatureProperty::IsMessageSignatureTrusted
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IWSDSignatureProperty::IsMessageSignatureTrusted
 - wsdbase/IWSDSignatureProperty::IsMessageSignatureTrusted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSignatureProperty.IsMessageSignatureTrusted
---

# IWSDSignatureProperty::IsMessageSignatureTrusted


## -description

Specifies if a message signature is trusted.

## -parameters

### -param pbSignatureTrusted [out]

A pointer to a boolean that specifies if a message signature is trusted.

## -returns

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
Method succeeded.

</td>
</tr>
</table>

## -remarks

A message is trusted if the signing certificate is among one of the certificates or in the certificate store passed down by the calling application in the <a href="/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoveryprovider2">WSDCreateDiscoveryProvider2</a> call.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdsignatureproperty">IWSDSignatureProperty</a>