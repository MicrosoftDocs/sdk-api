---
UID: NN:xpsdigitalsignature.IXpsSignature
title: IXpsSignature
author: windows-sdk-content
description: Represents a single digital signature.
old-location: xps\ixpssignature.htm
old-project: printdocs
ms.assetid: 23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsSignature, IXpsSignature interface [XPS Documents and Packaging], IXpsSignature interface [XPS Documents and Packaging],described, xps.ixpssignature, xpsdigitalsignature/IXpsSignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsdigitalsignature.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_SIGN_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignature interface


## -description


Represents a single digital signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignature</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSignature</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e4af0aa3-8420-4297-993c-dda4d4f7cf61">GetCertificateEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a> interface, which enumerates the package certificates that are attached to the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98a656c7-714b-4b59-9289-e78dee795eaa">GetCustomObjectEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/e82caa1e-4cf8-457f-86d9-24f707544199">IOpcSignatureCustomObjectEnumerator</a> interface, which enumerates the custom objects of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcdbd3e0-a19a-448c-92b7-71720eff3386">GetCustomReferenceEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/632e5e53-1677-4b55-9085-0def97531a5d">GetPolicy</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> value that represents the signing policy used when the signature is created.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9debed66-6588-40b5-ab52-a3dba0ddef92">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed0c29e2-225b-4478-a8d7-d9ec28f8b1f4">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40a21fa3-cf71-4c0d-8343-83a2c1a216c9">GetSignatureValue</a>
</td>
<td align="left" width="63%">
Gets the encrypted hash value of the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e76487c-465c-4d15-82d0-ed2a21decc33">GetSignatureXml</a>
</td>
<td align="left" width="63%">
Gets the XML markup of the digital signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47edfe80-2111-4e87-bb11-056cf939bdd9">GetSigningTime</a>
</td>
<td align="left" width="63%">
Gets the date and time of signature creation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a75df35c-dd12-4217-a6f8-91401be46225">GetSigningTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the signing time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ba32f16-2e11-479c-bc3c-0982e90b883d">SetSignatureXml</a>
</td>
<td align="left" width="63%">
Sets the XML markup of the digital signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f3239dd-e29f-4340-a4ad-49ceb6a151de">Verify</a>
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




<a href="https://msdn.microsoft.com/a66ad728-9d20-44d9-a363-1d2a7927d810">IOpcCertificateEnumerator</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a>
 

 

