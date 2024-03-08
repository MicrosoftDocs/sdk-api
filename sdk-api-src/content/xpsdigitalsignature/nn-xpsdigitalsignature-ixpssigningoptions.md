---
UID: NN:xpsdigitalsignature.IXpsSigningOptions
title: IXpsSigningOptions (xpsdigitalsignature.h)
description: Provides access to the individual signing options that are used by new signatures.
helpviewer_keywords: ["IXpsSigningOptions","IXpsSigningOptions interface [XPS Documents and Packaging]","IXpsSigningOptions interface [XPS Documents and Packaging]","described","xps.ixpssigningoptions","xpsdigitalsignature/IXpsSigningOptions"]
old-location: xps\ixpssigningoptions.htm
tech.root: xps
ms.assetid: 71b9b348-1078-4f55-a071-e5e2f273f85c
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions, IXpsSigningOptions interface [XPS Documents and Packaging], IXpsSigningOptions interface [XPS Documents and Packaging],described, xps.ixpssigningoptions, xpsdigitalsignature/IXpsSigningOptions
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
 - IXpsSigningOptions
 - xpsdigitalsignature/IXpsSigningOptions
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
 - IXpsSigningOptions
---

# IXpsSigningOptions interface

## -description

Provides access to the individual signing options that are used by new signatures.

## -inheritance

The <b>IXpsSigningOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSigningOptions</b> also has these types of members:

## -members

The <b>IXpsSigningOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcertificateset">GetCertificateSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface, which can be used to add additional certificates to the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomobjects">GetCustomObjects</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomreferences">GetCustomReferences</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getdigestmethod">GetDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the current digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to be used for this signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getpolicy">GetPolicy</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that specifies the signing policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignatureid">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignaturemethod">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignaturepartname">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsigningtimeformat">GetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the signing time string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod">SetDigestMethod</a>
</td>
<td align="left" width="63%">
Sets the URI of the digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to use for this signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy">SetPolicy</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that represents the signing policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignatureid">SetSignatureId</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod">SetSignatureMethod</a>
</td>
<td align="left" width="63%">
Sets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturepartname">SetSignaturePartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsigningtimeformat">SetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the signing time string.

</td>
</tr>
</table>

## -members

The <b>IXpsSigningOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcertificateset">GetCertificateSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface, which can be used to add additional certificates to the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomobjects">GetCustomObjects</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomreferences">GetCustomReferences</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getdigestmethod">GetDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the current digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to be used for this signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getpolicy">GetPolicy</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that specifies the signing policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignatureid">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignaturemethod">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsignaturepartname">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getsigningtimeformat">GetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the signing time string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod">SetDigestMethod</a>
</td>
<td align="left" width="63%">
Sets the URI of the digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value that specifies the signing flags to use for this signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy">SetPolicy</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that represents the signing policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignatureid">SetSignatureId</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod">SetSignatureMethod</a>
</td>
<td align="left" width="63%">
Sets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturepartname">SetSignaturePartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsigningtimeformat">SetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the signing time string.

</td>
</tr>
</table>

## -remarks

To create a new instance of this interface, call <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>.

When a new instance of this interface is returned by <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod  properties are not initialized. These properties  must be initialized before the new interface can be used as a parameter of the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
