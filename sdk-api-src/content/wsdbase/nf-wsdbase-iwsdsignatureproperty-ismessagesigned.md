---
UID: NF:wsdbase.IWSDSignatureProperty.IsMessageSigned
title: IWSDSignatureProperty::IsMessageSigned (wsdbase.h)
description: Specifies if a message is signed.
helpviewer_keywords: ["IWSDSignatureProperty interface","IsMessageSigned method","IWSDSignatureProperty.IsMessageSigned","IWSDSignatureProperty::IsMessageSigned","IsMessageSigned","IsMessageSigned method","IsMessageSigned method","IWSDSignatureProperty interface","ncd.iwsdsignatureproperty_ismessagesigned","wsdbase/IWSDSignatureProperty::IsMessageSigned"]
old-location: ncd\iwsdsignatureproperty_ismessagesigned.htm
tech.root: ncd
ms.assetid: ca91bb1e-b8a6-4cfe-850c-887b39ae239e
ms.date: 12/05/2018
ms.keywords: IWSDSignatureProperty interface,IsMessageSigned method, IWSDSignatureProperty.IsMessageSigned, IWSDSignatureProperty::IsMessageSigned, IsMessageSigned, IsMessageSigned method, IsMessageSigned method,IWSDSignatureProperty interface, ncd.iwsdsignatureproperty_ismessagesigned, wsdbase/IWSDSignatureProperty::IsMessageSigned
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
 - IWSDSignatureProperty::IsMessageSigned
 - wsdbase/IWSDSignatureProperty::IsMessageSigned
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
 - IWSDSignatureProperty.IsMessageSigned
---

# IWSDSignatureProperty::IsMessageSigned


## -description

Specifies if a message is signed.

## -parameters

### -param pbSigned [out]

A pointer to a boolean that specifies if a message signature is signed.

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

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdsignatureproperty">IWSDSignatureProperty</a>