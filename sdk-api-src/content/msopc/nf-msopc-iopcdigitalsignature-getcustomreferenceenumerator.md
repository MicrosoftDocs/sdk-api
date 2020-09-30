---
UID: NF:msopc.IOpcDigitalSignature.GetCustomReferenceEnumerator
title: IOpcDigitalSignature::GetCustomReferenceEnumerator (msopc.h)
description: Gets an enumerator of the IOpcSignatureReference interface pointers that represent references to application-specific XML elements that have been signed.
helpviewer_keywords: ["GetCustomReferenceEnumerator","GetCustomReferenceEnumerator method [Open Packaging Conventions]","GetCustomReferenceEnumerator method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetCustomReferenceEnumerator method","IOpcDigitalSignature.GetCustomReferenceEnumerator","IOpcDigitalSignature::GetCustomReferenceEnumerator","msopc/IOpcDigitalSignature::GetCustomReferenceEnumerator","opc.iopcdigitalsignature_getcustomreferenceenumerator"]
old-location: opc\iopcdigitalsignature_getcustomreferenceenumerator.htm
tech.root: OPC
ms.assetid: 8cc5ae5d-faef-451d-8ad8-db4b8b5c0e22
ms.date: 12/05/2018
ms.keywords: GetCustomReferenceEnumerator, GetCustomReferenceEnumerator method [Open Packaging Conventions], GetCustomReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetCustomReferenceEnumerator method, IOpcDigitalSignature.GetCustomReferenceEnumerator, IOpcDigitalSignature::GetCustomReferenceEnumerator, msopc/IOpcDigitalSignature::GetCustomReferenceEnumerator, opc.iopcdigitalsignature_getcustomreferenceenumerator
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
 - IOpcDigitalSignature::GetCustomReferenceEnumerator
 - msopc/IOpcDigitalSignature::GetCustomReferenceEnumerator
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
 - IOpcDigitalSignature.GetCustomReferenceEnumerator
---

# IOpcDigitalSignature::GetCustomReferenceEnumerator


## -description

Gets an enumerator of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers that represent references to application-specific XML elements that have been signed.

## -parameters

### -param customReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers.  An <b>IOpcSignatureReference</b> interface pointer represents a reference to an application-specific XML element that has been signed.

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
The <i>customReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To access the signed XML Element by using an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectenumerator-getcurrent">IOpcSignatureCustomObjectEnumerator::GetCurrent</a> method. To access the markup of the signed XML element, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobject-getxml">IOpcSignatureCustomObject::GetXml</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectenumerator">IOpcSignatureCustomObjectEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>