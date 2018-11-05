---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetIntent
title: IXpsSignatureRequest::GetIntent
author: windows-sdk-content
description: Sets the string that describes the intent or meaning of the signature.
old-location: xps\ixpssignaturerequest_getintent.htm
tech.root: printdocs
ms.assetid: d4da2d1b-e907-4498-a196-fd52742740b6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetIntent, GetIntent method [XPS Documents and Packaging], GetIntent method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetIntent method, IXpsSignatureRequest.GetIntent, IXpsSignatureRequest::GetIntent, xps.ixpssignaturerequest_getintent, xpsdigitalsignature/IXpsSignatureRequest::GetIntent
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
 - IXpsSignatureRequest.GetIntent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureRequest::GetIntent


## -description


Sets the string that describes the intent or meaning of the signature.


## -parameters




### -param intent [out, retval]

The signature intention agreement against which the signer is signing.


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
<i>intent</i> is <b>NULL</b>.

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



The signature intent string describes what the signature means to the signer. For example, for the  signature intent string "I have read and agree with the contents of this document" the presence of a digital signature means that the signer has read and agrees with the content of the document.

This method allocates the memory used by the string that is returned in <i>intent</i>.  If <i>intent</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

