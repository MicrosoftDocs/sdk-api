---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSigningTime
title: IXpsSignature::GetSigningTime
author: windows-sdk-content
description: Gets the date and time of signature creation.
old-location: xps\ixpssignature_getsigningtime.htm
old-project: printdocs
ms.assetid: 47edfe80-2111-4e87-bb11-056cf939bdd9
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetSigningTime, GetSigningTime method [XPS Documents and Packaging], GetSigningTime method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSigningTime method, IXpsSignature.GetSigningTime, IXpsSignature::GetSigningTime, xps.ixpssignature_getsigningtime, xpsdigitalsignature/IXpsSignature::GetSigningTime
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
 - IXpsSignature.GetSigningTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignature::GetSigningTime


## -description


Gets the date and time of signature creation.


## -parameters




### -param sigDateTimeString [out, retval]

A string that contains the date and time information.


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
</table>
 




## -remarks



The date-time string returned in <i>sigDateTimeString</i> is in a  W3C date-time format, which is described at <a href="http://go.microsoft.com/fwlink/p/?linkid=161711">http://www.w3.org/TR/NOTE-datetime</a>.

To get the specific format of the date-time string that is returned in <i>sigDateTimeString</i>, call <a href="https://msdn.microsoft.com/a75df35c-dd12-4217-a6f8-91401be46225">GetSigningTimeFormat</a>.

This method allocates the memory used by the string that is returned in <i>sigDateTimeString</i>.  If <i>sigDateTimeString</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

