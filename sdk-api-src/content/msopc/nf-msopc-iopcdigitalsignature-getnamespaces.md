---
UID: NF:msopc.IOpcDigitalSignature.GetNamespaces
title: IOpcDigitalSignature::GetNamespaces (msopc.h)
description: Gets the prefix and namespace mapping of the Signature element of the signature markup.
helpviewer_keywords: ["GetNamespaces","GetNamespaces method [Open Packaging Conventions]","GetNamespaces method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetNamespaces method","IOpcDigitalSignature.GetNamespaces","IOpcDigitalSignature::GetNamespaces","msopc/IOpcDigitalSignature::GetNamespaces","opc.iopcdigitalsignature_getnamespaces"]
old-location: opc\iopcdigitalsignature_getnamespaces.htm
tech.root: OPC
ms.assetid: c9360d23-1eac-4bb1-ae40-c157f1a79621
ms.date: 12/05/2018
ms.keywords: GetNamespaces, GetNamespaces method [Open Packaging Conventions], GetNamespaces method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetNamespaces method, IOpcDigitalSignature.GetNamespaces, IOpcDigitalSignature::GetNamespaces, msopc/IOpcDigitalSignature::GetNamespaces, opc.iopcdigitalsignature_getnamespaces
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
 - IOpcDigitalSignature::GetNamespaces
 - msopc/IOpcDigitalSignature::GetNamespaces
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
 - IOpcDigitalSignature.GetNamespaces
---

# IOpcDigitalSignature::GetNamespaces


## -description

Gets the prefix and namespace mapping of the <b>Signature</b> element of the signature markup.

## -parameters

### -param prefixes [out]

A pointer to a buffer of XML prefix strings. If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory of each string in the buffer and then to free the memory of the buffer itself.

### -param namespaces [out]

A pointer to a buffer of XML namespace strings. If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory of each string in the buffer and then to free the memory of the buffer itself.

### -param count [out]

The size of the <i>prefixes</i> and <i>namespaces</i> buffers.

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
The <i>prefixes</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>namespaces</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>count</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <i>prefixes</i> and <i>namespaces</i> buffers are mapped to each other by index.

This method allocates memory used by the buffers returned in <i>prefixes</i> and <i>namespaces</i> and the strings contained in each buffer.


#### Examples

The following code shows how to use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the memory of the buffers and the strings they contain.


```cpp
// Prepare to call GetNamespaces
LPWSTR* prefixes = NULL;
LPWSTR* namespaces = NULL;
UINT32 count = 0;

// Call to GetNamespaces succeeds
if ( SUCCEEDED( signature->GetNamespaces(&prefixes, &namespaces, &count) ) )
{
    // Process strings in prefixes and namespaces as needed for the application

    // Free memory for each string
    for (UINT32 i = 0; i < count; i++)
    {
        CoTaskMemFree(prefixes[i]);
        CoTaskMemFree(namespaces[i]);
    }
    // Free memory for the buffers
    CoTaskMemFree(prefixes);
    CoTaskMemFree(namespaces);
}
```

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