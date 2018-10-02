---
UID: NN:xpsdigitalsignature.IXpsSignatureBlock
title: IXpsSignatureBlock
author: windows-sdk-content
description: Represents a block of signature requests that are stored in a SignatureDefinitions part.
old-location: xps\ixpssignatureblock.htm
tech.root: printdocs
ms.assetid: cb2b7fe2-f3d9-4542-958f-5412d2498a9f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsSignatureBlock, IXpsSignatureBlock interface [XPS Documents and Packaging], IXpsSignatureBlock interface [XPS Documents and Packaging],described, xps.ixpssignatureblock, xpsdigitalsignature/IXpsSignatureBlock
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
 - IXpsSignatureBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureBlock interface


## -description


Represents a block of signature requests  that are  stored in a SignatureDefinitions part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignatureBlock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSignatureBlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSignatureBlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73b9e0b4-a650-4886-bafb-828a659b8446">CreateRequest</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface and adds it to the signature block.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e9052d9-9a27-41fe-8842-50033cb8edf2">GetDocumentIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the FixedDocument part that references the SignatureDefinitions part that corresponds to this signature block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f93e94ff-c56f-4b3c-8af8-983253bd5657">GetDocumentName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the  <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the URI of the document part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43dbb5f5-d69b-435e-8ace-54615796871d">GetPartName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the URI of the SignatureDefinitions part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97050917-8b41-4e4f-80c5-d8f166897c96">GetRequests</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/bb8279e1-a98b-4156-8b90-d9b69411bfa3">IXpsSignatureRequestCollection</a> interface that contains a collection of signature requests.
            

</td>
</tr>
</table> 


## -remarks



This interface cannot exist independently from the signature manager from which it was instantiated.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="https://msdn.microsoft.com/bb8279e1-a98b-4156-8b90-d9b69411bfa3">IXpsSignatureRequestCollection</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

