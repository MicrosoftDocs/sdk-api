---
UID: NN:xpsdigitalsignature.IXpsSignatureRequest
title: IXpsSignatureRequest
author: windows-sdk-content
description: Accesses the components of a signature request.
old-location: xps\ixpssignaturerequest.htm
tech.root: printdocs
ms.assetid: 5ece2402-ab0e-4695-b9d7-478a65199ec8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsSignatureRequest, IXpsSignatureRequest interface [XPS Documents and Packaging], IXpsSignatureRequest interface [XPS Documents and Packaging],described, xps.ixpssignaturerequest, xpsdigitalsignature/IXpsSignatureRequest
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsSignatureRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureRequest interface


## -description


Accesses the components of a signature request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignatureRequest</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSignatureRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSignatureRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4da2d1b-e907-4498-a196-fd52742740b6">GetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbe5872e-76af-4aa1-86ad-ed7c36fd6447">GetRequestedSigner</a>
</td>
<td align="left" width="63%">
Gets the identity of the person who has signed or is requesting to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abca5fdf-258b-4ce8-8b29-eae9a6d17cd7">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier of  the signature request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14cbe79d-a299-4e8d-9734-8571c0b535ce">GetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Gets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/649ab92f-9195-47a9-8a02-546825245e2b">GetSignature</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76b2d0a5-2d62-455d-8822-88ca14a497ae">GetSigningLocale</a>
</td>
<td align="left" width="63%">
Gets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a93c77-c978-4483-b0e0-36d998add184">GetSpotLocation</a>
</td>
<td align="left" width="63%">
Gets the page and the location on the page where the visible digital signature or the digital signature request will be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a77a168-58c7-4bb4-83ee-ed4dfd2839fe">SetIntent</a>
</td>
<td align="left" width="63%">
Sets the string that describes the intent or meaning of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c744fb64-2e94-484c-9045-46a8357b0007">SetRequestedSigner</a>
</td>
<td align="left" width="63%">
Sets the identity of the person who signed or is requested to sign the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7048b34-17f8-4df4-b1c6-6c6e6250f02a">SetRequestSignByDate</a>
</td>
<td align="left" width="63%">
Sets the date and time before which the requested signer must sign the specified parts of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03d93f1a-2d49-4179-b706-20a688e2467d">SetSigningLocale</a>
</td>
<td align="left" width="63%">
Sets the legal jurisdiction of the package signing location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ee13dd-ceea-4cd3-8c9e-4300c0c304ab">SetSpotLocation</a>
</td>
<td align="left" width="63%">
Specifies the page and the  location on the page  where   the visible digital signature or the digital signature request  will be displayed.

</td>
</tr>
</table> 


## -remarks



The <b>IXpsSignatureRequest</b> interface corresponds to a single <b>SignatureDefinition</b> element in the markup of the SignatureDefinitons part.

This <b>SignatureDefinition</b> element markup is described in section 10.2.2 of the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>. 

All signature requests are 
stored in a request collection of a signature block. They cannot exist independently from the <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface from which they were instantiated.




## -see-also




<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

