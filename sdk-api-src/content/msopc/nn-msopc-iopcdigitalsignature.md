---
UID: NN:msopc.IOpcDigitalSignature
title: IOpcDigitalSignature (msopc.h)
author: windows-sdk-content
description: Represents a package digital signature.
old-location: opc\iopcdigitalsignature.htm
tech.root: OPC
ms.assetid: cfa38ef6-9d96-4577-a3bf-518784d19ad8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignature, IOpcDigitalSignature interface [Open Packaging Conventions], IOpcDigitalSignature interface [Open Packaging Conventions],described, msopc/IOpcDigitalSignature, opc.iopcdigitalsignature
ms.topic: interface
f1_keywords: 
 - "msopc/IOpcDigitalSignature"
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
 - IOpcDigitalSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcDigitalSignature interface


## -description


Represents a  package digital signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcDigitalSignature</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcDigitalSignature</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcDigitalSignature</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcanonicalizationmethod">GetCanonicalizationMethod</a>
</td>
<td align="left" width="63%">
Gets the canonicalization method  that was applied to the <b>SignedInfo</b> element of the serialized signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcertificateenumerator">GetCertificateEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of certificates that are used in the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcustomobjectenumerator">GetCustomObjectEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers that represent application-specific <b>Object</b> elements in the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcustomreferenceenumerator">GetCustomReferenceEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers that represent references to application-specific XML elements that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getnamespaces">GetNamespaces</a>
</td>
<td align="left" width="63%">
Gets the prefix and namespace mapping of the <b>Signature</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getpackageobjectreference">GetPackageObjectReference</a>
</td>
<td align="left" width="63%">
Gets an  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignatureid">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturemethod">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method used to calculate the value in the <b>SignatureValue</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturepartname">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the part that contains the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturepartreferenceenumerator">GetSignaturePartReferenceEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturerelationshipreferenceenumerator">GetSignatureRelationshipReferenceEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturevalue">GetSignatureValue</a>
</td>
<td align="left" width="63%">
Gets the decoded value in the <b>SignatureValue</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturexml">GetSignatureXml</a>
</td>
<td align="left" width="63%">
Gets the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">GetSigningTime</a>
</td>
<td align="left" width="63%">
Gets a string that indicates the time at which the signature was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-gettimeformat">GetTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the string returned by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">GetSigningTime</a> method.
            

</td>
</tr>
</table> 


## -remarks



To generate a signature and create an   <b>IOpcDigitalSignature</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> method.

To access generated signature by using an   <b>IOpcDigitalSignature</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignatureenumerator-getcurrent">IOpcDigitalSignatureEnumerator::GetCurrent</a> method.

When a signature is generated, this information is serialized in the XML markup of the signature (signature markup).  The signature markup that results is stored in a signature part.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignatureenumerator">IOpcDigitalSignatureEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

