---
UID: NF:msopc.IOpcDigitalSignature.GetPackageObjectReference
title: IOpcDigitalSignature::GetPackageObjectReference (msopc.h)
description: Gets an IOpcSignatureReference interface pointer that represents the reference to the package-specific Object element that has been signed.
helpviewer_keywords: ["GetPackageObjectReference","GetPackageObjectReference method [Open Packaging Conventions]","GetPackageObjectReference method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetPackageObjectReference method","IOpcDigitalSignature.GetPackageObjectReference","IOpcDigitalSignature::GetPackageObjectReference","msopc/IOpcDigitalSignature::GetPackageObjectReference","opc.iopcdigitalsignature_getpackageobjectreference"]
old-location: opc\iopcdigitalsignature_getpackageobjectreference.htm
tech.root: OPC
ms.assetid: 67f4404f-518c-4a47-8c8e-b5b8d13e18cb
ms.date: 12/05/2018
ms.keywords: GetPackageObjectReference, GetPackageObjectReference method [Open Packaging Conventions], GetPackageObjectReference method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetPackageObjectReference method, IOpcDigitalSignature.GetPackageObjectReference, IOpcDigitalSignature::GetPackageObjectReference, msopc/IOpcDigitalSignature::GetPackageObjectReference, opc.iopcdigitalsignature_getpackageobjectreference
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
 - IOpcDigitalSignature::GetPackageObjectReference
 - msopc/IOpcDigitalSignature::GetPackageObjectReference
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
 - IOpcDigitalSignature.GetPackageObjectReference
---

# IOpcDigitalSignature::GetPackageObjectReference


## -description

Gets an  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.

## -parameters

### -param packageObjectReference [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.

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
The <i>packageObjectReference</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The   <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>   interface pointer received in the <i>packageObjectReference</i> parameter represents the <b>Reference</b> element that has the  <b>URI</b> attribute value set to "#idPackageObject". The <b>URI</b> attribute value of this element is the <b>Id</b> attribute value of the package-specific <b>Object</b> element, prefixed with a pound sign ("#").

When the signature is generated and serialized as signature markup, the reference and the referenced  package-specific <b>Object</b> element are signed. The following markup shows the package-specific <b>Reference</b> element and the package-specific <b>Object</b> element in the resultant signature markup.


```xml
<!-- Signature markup. -->
<Signature>
    <SignedInfo>
        [...]
        <!-- A reference to the package-specific <Object> that
        is, or will be, signed. -->
        <Reference URI="#idPackageObject">
             [...]
        </Reference>
    </SignedInfo>
    [...]
    <!-- The package-specific <Object> element. -->
    <Object Id="idPackageObject">
        <!-- This element contains the <Reference> elements that
        refer to parts and relationships in the package that are
        or will be signed. -->
        <Manifest>
            [...] 
        </Manifest>
    </Object>
</Signature>
```



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