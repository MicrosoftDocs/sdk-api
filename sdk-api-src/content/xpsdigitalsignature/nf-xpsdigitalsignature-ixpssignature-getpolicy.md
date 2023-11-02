---
UID: NF:xpsdigitalsignature.IXpsSignature.GetPolicy
title: IXpsSignature::GetPolicy (xpsdigitalsignature.h)
description: Gets the XPS_SIGN_POLICY value that represents the signing policy used when the signature is created.
helpviewer_keywords: ["GetPolicy","GetPolicy method [XPS Documents and Packaging]","GetPolicy method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetPolicy method","IXpsSignature.GetPolicy","IXpsSignature::GetPolicy","xps.ixpssignature_getpolicy","xpsdigitalsignature/IXpsSignature::GetPolicy"]
old-location: xps\ixpssignature_getpolicy.htm
tech.root: xps
ms.assetid: 632e5e53-1677-4b55-9085-0def97531a5d
ms.date: 12/05/2018
ms.keywords: GetPolicy, GetPolicy method [XPS Documents and Packaging], GetPolicy method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetPolicy method, IXpsSignature.GetPolicy, IXpsSignature::GetPolicy, xps.ixpssignature_getpolicy, xpsdigitalsignature/IXpsSignature::GetPolicy
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignature::GetPolicy
 - xpsdigitalsignature/IXpsSignature::GetPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignature.GetPolicy
---

# IXpsSignature::GetPolicy


## -description

Gets the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that represents the signing policy used when the signature is created.

## -parameters

### -param policy [out, retval]

The logical <b>OR</b> of the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> values that represent the signing policy.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>policy</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>

## -remarks

The signing policy value that is returned in <i>policy</i> is determined by examining the signed parts and relationships in the document.

This method deduces the signature policy by examining the list of signed parts and relationships.
    For example, the <b>XPS_SIGN_POLICY_DISCARD_CONTROL</b> flag is set if the discard-control relationship type from the XPS package root is signed.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a>