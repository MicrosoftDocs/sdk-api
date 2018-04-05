---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.GetSignatureBlocks
title: IXpsSignatureManager::GetSignatureBlocks method
author: windows-driver-content
description: Gets a pointer to an IXpsSignatureBlockCollection interface that contains a collection of signature blocks.
old-location: xps\ixpssignaturemanager_getsignatureblocks.htm
old-project: printdocs
ms.assetid: 6f7ba22f-7c3b-47bf-8cb5-2e4e4a548dc2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetSignatureBlocks method [XPS Documents and Packaging], GetSignatureBlocks method [XPS Documents and Packaging], IXpsSignatureManager interface, GetSignatureBlocks,IXpsSignatureManager.GetSignatureBlocks, IXpsSignatureManager, IXpsSignatureManager interface [XPS Documents and Packaging], GetSignatureBlocks method, IXpsSignatureManager::GetSignatureBlocks, xps.ixpssignaturemanager_getsignatureblocks, xpsdigitalsignature/IXpsSignatureManager::GetSignatureBlocks
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
req.typenames: XPS_SIGN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsdigitalsignature.h
api_name:
-	IXpsSignatureManager.GetSignatureBlocks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureManager::GetSignatureBlocks method


## -description


Gets a pointer to an  <a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.


## -parameters




### -param signatureBlocks [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>signatureBlocks</i> is <b>NULL</b>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

