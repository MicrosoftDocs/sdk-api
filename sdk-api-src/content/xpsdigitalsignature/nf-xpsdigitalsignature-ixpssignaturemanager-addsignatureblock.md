---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.AddSignatureBlock
title: IXpsSignatureManager::AddSignatureBlock
author: windows-sdk-content
description: Creates a new IXpsSignatureBlock interface and adds it to the signature block collection.
old-location: xps\ixpssignaturemanager_addsignatureblock.htm
tech.root: printdocs
ms.assetid: a299882f-b9f4-4297-8438-e92d148a4014
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddSignatureBlock, AddSignatureBlock method [XPS Documents and Packaging], AddSignatureBlock method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],AddSignatureBlock method, IXpsSignatureManager.AddSignatureBlock, IXpsSignatureManager::AddSignatureBlock, xps.ixpssignaturemanager_addsignatureblock, xpsdigitalsignature/IXpsSignatureManager::AddSignatureBlock
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
 - IXpsSignatureManager.AddSignatureBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsdigitalsignature.h
: 
- IXpsSignatureManager.AddSignatureBlock
: 
---

# IXpsSignatureManager::AddSignatureBlock


## -description


Creates a new <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface and adds it to the signature block collection.


## -parameters




### -param partName [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the URI of the new part. For the method to generate a part name, this parameter can be set to <b>NULL</b>.


### -param fixedDocumentIndex [in]

The index value of the FixedDocument part with which the new signature block is to be associated.


### -param signatureBlock [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface. If access to the new interface is not required, this parameter can be set to <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>fixedDocumentIndex</i> references a fixed document that is not found in the XPS package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>
 




## -remarks



A signature block represents a SignatureDefinitions part in an XPS package. According to section 10.2.2 in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>,  zero or more SignatureDefinitions parts can be attached to each FixedDocument.
     This method creates a new SignatureDefinitions part with the specified name,   links it from the specified FixedDocument part by a relationship, 
    creates a new  <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface, and adds this new  interface to the internal signature block collection.

To retrieve a signature block, call   the <a href="https://msdn.microsoft.com/6f7ba22f-7c3b-47bf-8cb5-2e4e4a548dc2">GetSignatureBlocks</a> method.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

