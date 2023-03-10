---
UID: NF:msopc.IOpcSigningOptions.GetTimeFormat
title: IOpcSigningOptions::GetTimeFormat (msopc.h)
description: Gets the format of the string retrieved by the IOpcDigitalSignature::GetSigningTime method.
helpviewer_keywords: ["GetTimeFormat","GetTimeFormat method [Open Packaging Conventions]","GetTimeFormat method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetTimeFormat method","IOpcSigningOptions.GetTimeFormat","IOpcSigningOptions::GetTimeFormat","msopc/IOpcSigningOptions::GetTimeFormat","opc.iopcsigningoptions_gettimeformat"]
old-location: opc\iopcsigningoptions_gettimeformat.htm
tech.root: OPC
ms.assetid: 69394df9-5382-49eb-9aa2-0785dee10ac4
ms.date: 12/05/2018
ms.keywords: GetTimeFormat, GetTimeFormat method [Open Packaging Conventions], GetTimeFormat method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetTimeFormat method, IOpcSigningOptions.GetTimeFormat, IOpcSigningOptions::GetTimeFormat, msopc/IOpcSigningOptions::GetTimeFormat, opc.iopcsigningoptions_gettimeformat
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
 - IOpcSigningOptions::GetTimeFormat
 - msopc/IOpcSigningOptions::GetTimeFormat
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
 - IOpcSigningOptions.GetTimeFormat
---

# IOpcSigningOptions::GetTimeFormat


## -description

Gets the format of the string retrieved by the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.

## -parameters

### -param timeFormat [out, retval]

The value that describes the format of the <i>signingTime</i> parameter of <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">GetSigningTime</a>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>timeFormat</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The default format of the signing time string is <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>. To change the format of the signing time string, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-settimeformat">IOpcSigningOptions::SetTimeFormat</a> method.

To access the format of the signing time string after the signature has been generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-gettimeformat">IOpcDigitalSignature::GetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>