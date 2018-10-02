---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.CreateRequest
title: IXpsSignatureBlock::CreateRequest
author: windows-sdk-content
description: Creates a new IXpsSignatureRequest interface and adds it to the signature block.
old-location: xps\ixpssignatureblock_createrequest.htm
tech.root: printdocs
ms.assetid: 73b9e0b4-a650-4886-bafb-828a659b8446
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateRequest, CreateRequest method [XPS Documents and Packaging], CreateRequest method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],CreateRequest method, IXpsSignatureBlock.CreateRequest, IXpsSignatureBlock::CreateRequest, xps.ixpssignatureblock_createrequest, xpsdigitalsignature/IXpsSignatureBlock::CreateRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsSignatureBlock.CreateRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureBlock::CreateRequest


## -description


Creates a new <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface and adds it to the signature block.


## -parameters




### -param requestId [in]

A string that uniquely identifies the new signature request within the signature block. For the method to generate an ID string, set this parameter to <b>NULL</b>.


### -param signatureRequest [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface. If access to the new request interface is not  required, this parameter can be set to <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Either the interface is not connected to the signature manager, or <i>requestId</i> is <b>NULL</b> and a unique ID string could not be generated.

</td>
</tr>
</table>
 




## -remarks



The new signature request must have a unique request ID; no two  requests may have the same  ID string. 

Creating a new request marks the signature block as <i>dirty</i> and  generates new content for the SignatureDefinitions part. When the XPS package is serialized, the  new content will overwrite the previous content in the SignatureDefinitions part.




## -see-also




<a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

