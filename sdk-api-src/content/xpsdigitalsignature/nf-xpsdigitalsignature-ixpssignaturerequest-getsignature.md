---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetSignature
title: IXpsSignatureRequest::GetSignature method
author: windows-driver-content
description: Gets a pointer to an IXpsSignature interface that contains the XPS digital signature with the same unique identifier as the signature request.
old-location: xps\ixpssignaturerequest_getsignature.htm
old-project: printdocs
ms.assetid: 649ab92f-9195-47a9-8a02-546825245e2b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetSignature method [XPS Documents and Packaging], GetSignature method [XPS Documents and Packaging], IXpsSignatureRequest interface, GetSignature,IXpsSignatureRequest.GetSignature, IXpsSignatureRequest, IXpsSignatureRequest interface [XPS Documents and Packaging], GetSignature method, IXpsSignatureRequest::GetSignature, xps.ixpssignaturerequest_getsignature, xpsdigitalsignature/IXpsSignatureRequest::GetSignature
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
-	IXpsSignatureRequest.GetSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureRequest::GetSignature method


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request.


## -parameters




### -param signature [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request. If no matching signature is found, a <b>NULL</b> pointer is returned.


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
<i>signature</i> is <b>NULL</b>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

