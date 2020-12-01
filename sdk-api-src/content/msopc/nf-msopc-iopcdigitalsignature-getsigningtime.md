---
UID: NF:msopc.IOpcDigitalSignature.GetSigningTime
title: IOpcDigitalSignature::GetSigningTime (msopc.h)
description: Gets a string that indicates the time at which the signature was generated.
helpviewer_keywords: ["GetSigningTime","GetSigningTime method [Open Packaging Conventions]","GetSigningTime method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSigningTime method","IOpcDigitalSignature.GetSigningTime","IOpcDigitalSignature::GetSigningTime","msopc/IOpcDigitalSignature::GetSigningTime","opc.iopcdigitalsignature_getsigningtime"]
old-location: opc\iopcdigitalsignature_getsigningtime.htm
tech.root: OPC
ms.assetid: 8054eba8-ca53-42e4-9105-ef7cf20637c1
ms.date: 12/05/2018
ms.keywords: GetSigningTime, GetSigningTime method [Open Packaging Conventions], GetSigningTime method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSigningTime method, IOpcDigitalSignature.GetSigningTime, IOpcDigitalSignature::GetSigningTime, msopc/IOpcDigitalSignature::GetSigningTime, opc.iopcdigitalsignature_getsigningtime
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
 - IOpcDigitalSignature::GetSigningTime
 - msopc/IOpcDigitalSignature::GetSigningTime
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
 - IOpcDigitalSignature.GetSigningTime
---

# IOpcDigitalSignature::GetSigningTime


## -description

Gets a string that indicates the time at which the signature was generated.

## -parameters

### -param signingTime [out, retval]

A pointer to a string that indicates the time at which the signature was generated.

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
The <i>signingTime</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>signingTime</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

To get the format of the <i>signingTime </i> string, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-gettimeformat">GetTimeFormat</a> method.

<div class="alert"><b>Caution</b>  This is not a trusted time stamp.</div>
<div> </div>

#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>