---
UID: NF:xpsdigitalsignature.IXpsSignature.SetSignatureXml
title: IXpsSignature::SetSignatureXml
author: windows-sdk-content
description: Sets the XML markup of the digital signature.
old-location: xps\ixpssignature_setsignaturexml.htm
old-project: printdocs
ms.assetid: 3ba32f16-2e11-479c-bc3c-0982e90b883d
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsSignature interface [XPS Documents and Packaging],SetSignatureXml method, IXpsSignature.SetSignatureXml, IXpsSignature::SetSignatureXml, SetSignatureXml, SetSignatureXml method [XPS Documents and Packaging], SetSignatureXml method [XPS Documents and Packaging],IXpsSignature interface, xps.ixpssignature_setsignaturexml, xpsdigitalsignature/IXpsSignature::SetSignatureXml
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsSignature.SetSignatureXml
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignature::SetSignatureXml


## -description


Sets the XML markup of the digital signature.


## -parameters




### -param signatureXml [in]

The XML markup of the digital signature.


### -param count [in]

The size, in bytes, of the buffer referenced by <i>signatureXml</i>.


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
<i>signatureXml</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, the application must check that the signature markup is valid. If the signature markup is not valid, this method will fail and the content of the signature part will not be changed.

<div class="alert"><b>Warning</b>  <p class="note">Using this method to create digital signatures might cause other methods of this interface to return signatures and data that are no longer valid.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

