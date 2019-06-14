---
UID: NN:xpsdigitalsignature.IXpsSignature
title: IXpsSignature (xpsdigitalsignature.h)
author: windows-sdk-content
description: Represents a single digital signature.
old-location: xps\ixpssignature.htm
tech.root: printdocs
ms.assetid: 23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsSignature, IXpsSignature interface [XPS Documents and Packaging], IXpsSignature interface [XPS Documents and Packaging],described, xps.ixpssignature, xpsdigitalsignature/IXpsSignature
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignature interface


## -description


Represents a single digital signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignature</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignature</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSignature</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator">GetCertificateEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface, which enumerates the package certificates that are attached to the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcustomobjectenumerator">GetCustomObjectEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectenumerator">IOpcSignatureCustomObjectEnumerator</a> interface, which enumerates the custom objects of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcustomreferenceenumerator">GetCustomReferenceEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getpolicy">GetPolicy</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a> value that represents the signing policy used when the signature is created.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsignatureid">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsignaturepartname">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsignaturevalue">GetSignatureValue</a>
</td>
<td align="left" width="63%">
Gets the encrypted hash value of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsignaturexml">GetSignatureXml</a>
</td>
<td align="left" width="63%">
Gets the XML markup of the digital signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsigningtime">GetSigningTime</a>
</td>
<td align="left" width="63%">
Gets the date and time of signature creation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsigningtimeformat">GetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the signing time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-setsignaturexml">SetSignatureXml</a>
</td>
<td align="left" width="63%">
Sets the XML markup of the digital signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify">Verify</a>
</td>
<td align="left" width="63%">
Verifies the signature against a specified X.509 certificate.

</td>
</tr>
</table> 


## -remarks



This interface is linked to the signature manager from which it was instantiated and it cannot exist independently.

An <b>IXpsSignature</b> interface may represent a signature that is not XPS compliant. For example, it could represent a signature that includes only custom parts, which is not allowed by the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a>
 

 

