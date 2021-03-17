---
UID: NF:msopc.IOpcSigningOptions.SetTimeFormat
title: IOpcSigningOptions::SetTimeFormat (msopc.h)
description: Sets the format of the string retrieved by the IOpcDigitalSignature::GetSigningTime method.
helpviewer_keywords: ["IOpcSigningOptions interface [Open Packaging Conventions]","SetTimeFormat method","IOpcSigningOptions.SetTimeFormat","IOpcSigningOptions::SetTimeFormat","SetTimeFormat","SetTimeFormat method [Open Packaging Conventions]","SetTimeFormat method [Open Packaging Conventions]","IOpcSigningOptions interface","msopc/IOpcSigningOptions::SetTimeFormat","opc.iopcsigningoptions_settimeformat"]
old-location: opc\iopcsigningoptions_settimeformat.htm
tech.root: OPC
ms.assetid: 3f8c1dbe-6347-4013-bda6-5e08c9d6921d
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetTimeFormat method, IOpcSigningOptions.SetTimeFormat, IOpcSigningOptions::SetTimeFormat, SetTimeFormat, SetTimeFormat method [Open Packaging Conventions], SetTimeFormat method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetTimeFormat, opc.iopcsigningoptions_settimeformat
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcSigningOptions::SetTimeFormat
 - msopc/IOpcSigningOptions::SetTimeFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSigningOptions.SetTimeFormat
---

# IOpcSigningOptions::SetTimeFormat


## -description

Sets the format of the string retrieved by the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.

## -parameters

### -param timeFormat [in]

The value that describes the format of the string retrieved by the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>timeFormat</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a> enumeration value.

</td>
</tr>
</table>

## -remarks

This method changes the format of the signing time string from the default format, <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>, to a format that is specified by the caller.

To access the format of the signing time string before the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-gettimeformat">IOpcSigningOptions::GetTimeFormat</a> method. To access the format after the signature has been generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-gettimeformat">IOpcDigitalSignature::GetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>