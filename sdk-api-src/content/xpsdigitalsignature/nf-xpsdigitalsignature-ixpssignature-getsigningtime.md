---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSigningTime
title: IXpsSignature::GetSigningTime (xpsdigitalsignature.h)
author: windows-sdk-content
description: Gets the date and time of signature creation.
old-location: xps\ixpssignature_getsigningtime.htm
tech.root: printdocs
ms.assetid: 47edfe80-2111-4e87-bb11-056cf939bdd9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSigningTime, GetSigningTime method [XPS Documents and Packaging], GetSigningTime method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSigningTime method, IXpsSignature.GetSigningTime, IXpsSignature::GetSigningTime, xps.ixpssignature_getsigningtime, xpsdigitalsignature/IXpsSignature::GetSigningTime
ms.topic: method
f1_keywords: 
 - "xpsdigitalsignature/IXpsSignature.GetSigningTime"
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
 - IXpsSignature.GetSigningTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignature::GetSigningTime


## -description


Gets the date and time of signature creation.


## -parameters




### -param sigDateTimeString [out, retval]

A string that contains the date and time information.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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

To get the specific format of the date-time string that is returned in <i>sigDateTimeString</i>, call <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getsigningtimeformat">GetSigningTimeFormat</a>.

This method allocates the memory used by the string that is returned in <i>sigDateTimeString</i>.  If <i>sigDateTimeString</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

