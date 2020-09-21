---
UID: NF:wsdbase.IWSDSignatureProperty.GetSignature
title: IWSDSignatureProperty::GetSignature (wsdbase.h)
description: Gets the signature of a message.
helpviewer_keywords: ["GetSignature","GetSignature method","GetSignature method","IWSDSignatureProperty interface","IWSDSignatureProperty interface","GetSignature method","IWSDSignatureProperty.GetSignature","IWSDSignatureProperty::GetSignature","ncd.iwsdsignatureproperty_getsignature","wsdbase/IWSDSignatureProperty::GetSignature"]
old-location: ncd\iwsdsignatureproperty_getsignature.htm
tech.root: ncd
ms.assetid: e13df6a4-f51f-4453-8482-563ff7c398c3
ms.date: 12/05/2018
ms.keywords: GetSignature, GetSignature method, GetSignature method,IWSDSignatureProperty interface, IWSDSignatureProperty interface,GetSignature method, IWSDSignatureProperty.GetSignature, IWSDSignatureProperty::GetSignature, ncd.iwsdsignatureproperty_getsignature, wsdbase/IWSDSignatureProperty::GetSignature
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
 - IWSDSignatureProperty::GetSignature
 - wsdbase/IWSDSignatureProperty::GetSignature
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
 - IWSDSignatureProperty.GetSignature
---

# IWSDSignatureProperty::GetSignature


## -description

Gets the signature of a message.

## -parameters

### -param pbSignature [out]

A pointer to a buffer that will be filled with the signature  of the message.

### -param pdwSignatureSize [in, out]

On input, the size of <i>pbSignature</i> in bytes. On output, <i>pdwSignatureSize</i> contains the actual size of the buffer that was written.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTAVAIL</b></dt>
</dl>
</td>
<td width="60%">
The message is not signed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbSignature</i> is not large enough to hold the information.  <i>pdwSignatureSize</i> now specifies the required buffer size.

</td>
</tr>
</table>

## -remarks

If <b>NULL</b> is passed to <i>pbSignature</i>, then <b>GetSignature</b> will return the size of the buffer to allocate in the <i>pdwSignatureSize</i> parameter.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdsignatureproperty">IWSDSignatureProperty</a>