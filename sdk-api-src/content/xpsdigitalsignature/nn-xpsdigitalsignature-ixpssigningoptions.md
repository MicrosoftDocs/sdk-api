---
UID: NN:xpsdigitalsignature.IXpsSigningOptions
title: IXpsSigningOptions
author: windows-sdk-content
description: Provides access to the individual signing options that are used by new signatures.
old-location: xps\ixpssigningoptions.htm
tech.root: printdocs
ms.assetid: 71b9b348-1078-4f55-a071-e5e2f273f85c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXpsSigningOptions, IXpsSigningOptions interface [XPS Documents and Packaging], IXpsSigningOptions interface [XPS Documents and Packaging],described, xps.ixpssigningoptions, xpsdigitalsignature/IXpsSigningOptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsSigningOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions interface


## -description


Provides access to the individual signing options that are used by new signatures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSigningOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSigningOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSigningOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40e96263-03dd-4fbe-8383-0c0bf1abd8c4">GetCertificateSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a> interface, which can be used to add additional certificates to the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a3f913-57f2-40e1-b886-6cefb9e42a83">GetCustomObjects</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a9ab939-4581-40a9-acd3-2afe02c5e201">GetCustomReferences</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8976719-970b-4598-8f1c-0ef2446ae12b">GetDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the current digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02d07300-e8f2-44fa-a562-5cec03af9a8c">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/36fa92d4-ffd4-4666-8d3e-02436e3bb464">XPS_SIGN_FLAGS</a> value that specifies the signing flags to be used for this signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0643ee4d-7991-4570-8dce-8166f007abc8">GetPolicy</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> value that specifies the signing policy.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebcb9f75-c9da-4559-9a9f-915b166801bf">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab01420f-c401-463a-a695-4594c1f579d3">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c5dfbda-0ceb-4694-bc5d-7e16e6f6d3bc">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79af4463-1651-44d2-9143-b1f922ba5cfb">GetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the signing time string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9f72cc4-38b2-4a91-8813-183483d47986">SetDigestMethod</a>
</td>
<td align="left" width="63%">
Sets the URI of the digest method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59467fd5-c462-4827-a4f8-e152df981ace">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/36fa92d4-ffd4-4666-8d3e-02436e3bb464">XPS_SIGN_FLAGS</a> value that specifies the signing flags to use for this signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e1738b3-f1ce-407e-bbaa-7f4c57e30028">SetPolicy</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> value that represents the signing policy.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/314199f2-15bc-4ede-b18c-96c1dbfe5367">SetSignatureId</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/318f0e08-2384-4fab-a181-6ff3070ea21f">SetSignatureMethod</a>
</td>
<td align="left" width="63%">
Sets the signature method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24addd5c-09a5-4f1b-90eb-c398aa7dd9a1">SetSignaturePartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the document's signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55ed2bb7-56d0-41d6-a8c3-dc0ff8cde7f8">SetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the signing time string.

</td>
</tr>
</table> 


## -remarks



To create a new instance of this interface, call <a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">IXpsSignatureManager::CreateSigningOptions</a>.

When a new instance of this interface is returned by <a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod  properties are not initialized. These properties  must be initialized before the new interface can be used as a parameter of the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

