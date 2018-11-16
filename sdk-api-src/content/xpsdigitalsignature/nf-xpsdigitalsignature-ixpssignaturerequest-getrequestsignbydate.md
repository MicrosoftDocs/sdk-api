---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetRequestSignByDate
title: IXpsSignatureRequest::GetRequestSignByDate
author: windows-sdk-content
description: Gets the date and time before which the requested signer must sign the specified parts of the document.
old-location: xps\ixpssignaturerequest_getrequestsignbydate.htm
tech.root: printdocs
ms.assetid: 14cbe79d-a299-4e8d-9734-8571c0b535ce
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRequestSignByDate, GetRequestSignByDate method [XPS Documents and Packaging], GetRequestSignByDate method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetRequestSignByDate method, IXpsSignatureRequest.GetRequestSignByDate, IXpsSignatureRequest::GetRequestSignByDate, xps.ixpssignaturerequest_getrequestsignbydate, xpsdigitalsignature/IXpsSignatureRequest::GetRequestSignByDate
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
 - IXpsSignatureRequest.GetRequestSignByDate
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
- IXpsSignatureRequest.GetRequestSignByDate
: 
---

# IXpsSignatureRequest::GetRequestSignByDate


## -description


Gets the date and time before which the requested signer must sign the specified parts of the document.


## -parameters




### -param dateString [out, retval]

A string that contains the date and time before which the requested signer must sign the specified parts of the document.

The string is formatted as either <code>YYYY-MM-DDThh:mmZ</code>,  which includes the UTC time zone offset, or <code>YYYY-MM-DDThh:mm</code>, which does not include the UTC time zone offset. For example, without the time zone offset, 7:30:29 P.M. on July 4, 2008 would be represented  as <code>2008-07-04T19:30:29</code>.


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
<i>dateString</i> is <b>NULL</b>.

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



This method allocates the memory used by the string that is returned in <i>dateString</i>.  If <i>dateString</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

