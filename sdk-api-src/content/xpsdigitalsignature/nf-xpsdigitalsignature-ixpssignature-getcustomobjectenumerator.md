---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCustomObjectEnumerator
title: IXpsSignature::GetCustomObjectEnumerator
author: windows-driver-content
description: Gets a pointer to an IOpcSignatureCustomObjectEnumerator interface, which enumerates the custom objects of the signature.
old-location: xps\ixpssignature_getcustomobjectenumerator.htm
old-project: printdocs
ms.assetid: 98a656c7-714b-4b59-9289-e78dee795eaa
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetCustomObjectEnumerator, GetCustomObjectEnumerator method [XPS Documents and Packaging], GetCustomObjectEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCustomObjectEnumerator method, IXpsSignature.GetCustomObjectEnumerator, IXpsSignature::GetCustomObjectEnumerator, xps.ixpssignature_getcustomobjectenumerator, xpsdigitalsignature/IXpsSignature::GetCustomObjectEnumerator
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
-	IXpsSignature.GetCustomObjectEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignature::GetCustomObjectEnumerator


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/e82caa1e-4cf8-457f-86d9-24f707544199">IOpcSignatureCustomObjectEnumerator</a> interface, which enumerates the custom objects of the signature.


## -parameters




### -param customObjectEnumerator [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface, which  enumerates the custom objects of the signature.


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
The interface is not connected to the signature manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_OBJECT_DETACHED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not associated with the signature manager.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

