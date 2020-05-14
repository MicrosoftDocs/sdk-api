---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSigningTimeFormat
title: IXpsSignature::GetSigningTimeFormat (xpsdigitalsignature.h)
description: Gets the format of the signing time.
helpviewer_keywords: ["GetSigningTimeFormat","GetSigningTimeFormat method [XPS Documents and Packaging]","GetSigningTimeFormat method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetSigningTimeFormat method","IXpsSignature.GetSigningTimeFormat","IXpsSignature::GetSigningTimeFormat","xps.ixpssignature_getsigningtimeformat","xpsdigitalsignature/IXpsSignature::GetSigningTimeFormat"]
old-location: xps\ixpssignature_getsigningtimeformat.htm
tech.root: printdocs
ms.assetid: a75df35c-dd12-4217-a6f8-91401be46225
ms.date: 12/05/2018
ms.keywords: GetSigningTimeFormat, GetSigningTimeFormat method [XPS Documents and Packaging], GetSigningTimeFormat method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSigningTimeFormat method, IXpsSignature.GetSigningTimeFormat, IXpsSignature::GetSigningTimeFormat, xps.ixpssignature_getsigningtimeformat, xpsdigitalsignature/IXpsSignature::GetSigningTimeFormat
f1_keywords:
- xpsdigitalsignature/IXpsSignature.GetSigningTimeFormat
dev_langs:
- c++
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
- IXpsSignature.GetSigningTimeFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignature::GetSigningTimeFormat


## -description


Gets the format of the signing time.


## -parameters




### -param timeFormat [out, retval]

The value of <a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a> that describes the format of the signing time.


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



For more information about the  format of the date-time string that is returned  in <i>timeFormat</i>, see <a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

