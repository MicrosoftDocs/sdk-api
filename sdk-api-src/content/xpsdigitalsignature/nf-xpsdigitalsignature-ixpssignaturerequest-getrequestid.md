---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetRequestId
title: IXpsSignatureRequest::GetRequestId
author: windows-sdk-content
description: Gets the unique identifier of the signature request.
old-location: xps\ixpssignaturerequest_getrequestid.htm
tech.root: printdocs
ms.assetid: abca5fdf-258b-4ce8-8b29-eae9a6d17cd7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRequestId, GetRequestId method [XPS Documents and Packaging], GetRequestId method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetRequestId method, IXpsSignatureRequest.GetRequestId, IXpsSignatureRequest::GetRequestId, xps.ixpssignaturerequest_getrequestid, xpsdigitalsignature/IXpsSignatureRequest::GetRequestId
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
 - IXpsSignatureRequest.GetRequestId
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
- IXpsSignatureRequest.GetRequestId
: 
---

# IXpsSignatureRequest::GetRequestId


## -description


Gets the unique identifier of  the signature request.


## -parameters




### -param requestId [out, retval]

The unique identifier of  the signature request.


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
<i>requestId</i> is <b>NULL</b>.

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



This method allocates the memory used by the string that is returned in <i>requestId</i>.  If <i>requestId</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.

 The <i>requestId</i> parameter receives the value of the <b>SpotID</b> attribute  of the <b>SignatureDefinition</b> element. The <b>SpotID</b> attribute  is required and should follow the xs:ID (XML ID) format; however, 
    existing SignatureDefinitions parts are not checked for adherence to the recommended format. Some XPS documents that were produced by Windows Presentation Foundation (WPF) applications may have an ID that starts with a digit.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

