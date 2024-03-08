---
UID: NN:xpsdigitalsignature.IXpsSignatureRequest
title: IXpsSignatureRequest (xpsdigitalsignature.h)
description: Accesses the components of a signature request.
helpviewer_keywords: ["IXpsSignatureRequest","IXpsSignatureRequest interface [XPS Documents and Packaging]","IXpsSignatureRequest interface [XPS Documents and Packaging]","described","xps.ixpssignaturerequest","xpsdigitalsignature/IXpsSignatureRequest"]
old-location: xps\ixpssignaturerequest.htm
tech.root: xps
ms.assetid: 5ece2402-ab0e-4695-b9d7-478a65199ec8
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequest, IXpsSignatureRequest interface [XPS Documents and Packaging], IXpsSignatureRequest interface [XPS Documents and Packaging],described, xps.ixpssignaturerequest, xpsdigitalsignature/IXpsSignatureRequest
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
 - IXpsSignatureRequest
 - xpsdigitalsignature/IXpsSignatureRequest
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
 - IXpsSignatureRequest
---

# IXpsSignatureRequest interface

## -description

Accesses the components of a signature request.

## -inheritance

The <b>IXpsSignatureRequest</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignatureRequest</b> also has these types of members:

## -members

The <b>IXpsSignatureRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getintent">GetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestedsigner">GetRequestedSigner</a>
</td>
<td align="left" width="63%">
Gets the identity of the person who has signed or is requesting to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestid">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier of  the signature request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestsignbydate">GetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Gets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getsignature">GetSignature</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getsigninglocale">GetSigningLocale</a>
</td>
<td align="left" width="63%">
Gets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getspotlocation">GetSpotLocation</a>
</td>
<td align="left" width="63%">
Gets the page and the location on the page where the visible digital signature or the digital signature request will be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent">SetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner">SetRequestedSigner</a>
</td>
<td align="left" width="63%">
Sets the identity of the person who signed or is requested to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate">SetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Sets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setsigninglocale">SetSigningLocale</a>
</td>
<td align="left" width="63%">
Sets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setspotlocation">SetSpotLocation</a>
</td>
<td align="left" width="63%">
Specifies the page and the  location on the page  where   the visible digital signature or the digital signature request  will be displayed.

</td>
</tr>
</table>

## -members

The <b>IXpsSignatureRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getintent">GetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestedsigner">GetRequestedSigner</a>
</td>
<td align="left" width="63%">
Gets the identity of the person who has signed or is requesting to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestid">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier of  the signature request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getrequestsignbydate">GetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Gets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getsignature">GetSignature</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getsigninglocale">GetSigningLocale</a>
</td>
<td align="left" width="63%">
Gets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-getspotlocation">GetSpotLocation</a>
</td>
<td align="left" width="63%">
Gets the page and the location on the page where the visible digital signature or the digital signature request will be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent">SetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner">SetRequestedSigner</a>
</td>
<td align="left" width="63%">
Sets the identity of the person who signed or is requested to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate">SetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Sets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setsigninglocale">SetSigningLocale</a>
</td>
<td align="left" width="63%">
Sets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setspotlocation">SetSpotLocation</a>
</td>
<td align="left" width="63%">
Specifies the page and the  location on the page  where   the visible digital signature or the digital signature request  will be displayed.

</td>
</tr>
</table>

## -remarks

The <b>IXpsSignatureRequest</b> interface corresponds to a single <b>SignatureDefinition</b> element in the markup of the SignatureDefinitons part.

This <b>SignatureDefinition</b> element markup is described in section 10.2.2 of the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>. 

All signature requests are 
stored in a request collection of a signature block. They cannot exist independently from the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface from which they were instantiated.

## -see-also

<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
