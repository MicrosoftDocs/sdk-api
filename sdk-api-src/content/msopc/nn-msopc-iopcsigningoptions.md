---
UID: NN:msopc.IOpcSigningOptions
title: IOpcSigningOptions (msopc.h)
description: Provides methods to set and access information required to generate a signature.helpviewer_keywords: ["IOpcSigningOptions","IOpcSigningOptions interface [Open Packaging Conventions]","IOpcSigningOptions interface [Open Packaging Conventions]","described","msopc/IOpcSigningOptions","opc.iopcsigningoptions"]
old-location: opc\iopcsigningoptions.htm
tech.root: OPC
ms.assetid: 5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions, IOpcSigningOptions interface [Open Packaging Conventions], IOpcSigningOptions interface [Open Packaging Conventions],described, msopc/IOpcSigningOptions, opc.iopcsigningoptions
f1_keywords:
- msopc/IOpcSigningOptions
dev_langs:
- c++
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msopc.h
api_name:
- IOpcSigningOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSigningOptions interface


## -description


Provides methods to set and access information required to generate a signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSigningOptions</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSigningOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSigningOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcertificateembeddingoption">GetCertificateEmbeddingOption</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the storage location in the package of the certificate to be used for the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcertificateset">GetCertificateSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomobjectset">GetCustomObjectSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomreferenceset">GetCustomReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getdefaultdigestmethod">GetDefaultDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the default digest method that will be used to compute digest values for objects to be signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignatureid">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturemethod">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method to use to calculate and encrypt the hash value of the <b>SignedInfo</b> element, which will be serialized as the <b>SignatureValue</b> element of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturepartname">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature part where the signature markup will be stored.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturepartreferenceset">GetSignaturePartReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturerelationshipreferenceset">GetSignatureRelationshipReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-gettimeformat">GetTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the string retrieved by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setcertificateembeddingoption">SetCertificateEmbeddingOption</a>
</td>
<td align="left" width="63%">
Set the storage location of the certificate to be used for the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">SetDefaultDigestMethod</a>
</td>
<td align="left" width="63%">
Sets the default digest method that will be used to compute digest values for objects to be signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignatureid">SetSignatureId</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">SetSignatureMethod</a>
</td>
<td align="left" width="63%">
Sets the signature method to use to calculate and encrypt the hash value of the <b>SignedInfo</b> element, which will be contained in the <b>SignatureValue</b> element of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturepartname">SetSignaturePartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the signature part where the signature markup will be stored.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-settimeformat">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the string retrieved by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.
            

</td>
</tr>
</table> 


## -remarks



To generate a signature, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> method with the <i>signingOptions</i> parameter value set to an <b>IOpcSigningOptions</b> interface pointer.

To create an <b>IOpcSigningOptions</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-createsigningoptions">IOpcDigitalSignatureManager::CreateSigningOptions</a> method.

The caller must set a default for the digest method and signature method before generating a signature. To set a default digest method, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">SetDefaultDigestMethod</a> method. To set a signature method, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">SetSignatureMethod</a> method.

To get an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomobjectset">GetCustomObjectSet</a> method. The interface pointers in the set represent application-specific <b>Object</b> elements.

 To get an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomreferenceset">GetCustomReferenceSet</a> method. The interface pointers in the set represent references to application-specific <b>Object</b> elements or their children that will be signed when the signature is generated.

The default location of the certificate is <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>. To change this value, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setcertificateembeddingoption">SetCertificateEmbeddingOption</a> method.

The default format of the signing time string is <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>. To change the format of the signing time string, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-settimeformat">SetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

