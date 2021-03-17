---
UID: NF:msopc.IOpcSignatureReference.GetUri
title: IOpcSignatureReference::GetUri (msopc.h)
description: Gets the URI of the referenced XML element.
helpviewer_keywords: ["GetUri","GetUri method [Open Packaging Conventions]","GetUri method [Open Packaging Conventions]","IOpcSignatureReference interface","IOpcSignatureReference interface [Open Packaging Conventions]","GetUri method","IOpcSignatureReference.GetUri","IOpcSignatureReference::GetUri","msopc/IOpcSignatureReference::GetUri","opc.iopcsignaturereference_geturi"]
old-location: opc\iopcsignaturereference_geturi.htm
tech.root: OPC
ms.assetid: 4dd02f48-9b49-4e74-b0cf-c51c0a594437
ms.date: 12/05/2018
ms.keywords: GetUri, GetUri method [Open Packaging Conventions], GetUri method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetUri method, IOpcSignatureReference.GetUri, IOpcSignatureReference::GetUri, msopc/IOpcSignatureReference::GetUri, opc.iopcsignaturereference_geturi
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
 - IOpcSignatureReference::GetUri
 - msopc/IOpcSignatureReference::GetUri
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
 - IOpcSignatureReference.GetUri
---

# IOpcSignatureReference::GetUri


## -description

Gets the URI of the referenced XML element.

## -parameters

### -param referenceUri [out, retval]

A pointer to the  URI of the referenced element.

This URI represented by a string is  "#" followed by  the <b>Id</b> attribute value of the referenced element: "#<i>&lt;elementIdValue&gt;</i>".

For examples, see the Remarks section.

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
The <i>referenceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The URI of the referenced element is serialized in the signature markup as the <b>URI</b> attribute of a <b>Reference</b> element.

The following table shows two examples of the <i>referenceUri</i> parameter value represented as strings.<table>
<tr>
<th><i>referenceUri</i> Value as String</th>
<th>Referenced Element</th>
<th>Element Description</th>
</tr>
<tr>
<td>"#<i>idMyCustomObject</i>"</td>
<td>"&lt;Object Id="<i>idMyCustomObject</i>"&gt;<i>...</i>&lt;/Object&gt;"</td>
<td>
An application-specific <b>Object</b> element.

</td>
</tr>
<tr>
<td>"#<i>idMyElement</i>"</td>
<td>"&lt;Object&gt;&lt;<i>MyElement</i> Id="<i>idMyElement</i>"&gt;<i>...</i>&lt;/<i>MyElement</i>&gt;...&lt;/Object&gt;"</td>
<td>
A child element of an application-specific <b>Object</b>.

</td>
</tr>
</table>
 




#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>