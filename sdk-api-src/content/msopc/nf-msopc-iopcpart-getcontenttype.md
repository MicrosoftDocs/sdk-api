---
UID: NF:msopc.IOpcPart.GetContentType
title: IOpcPart::GetContentType (msopc.h)
description: Gets the media type of part content.
helpviewer_keywords: ["GetContentType","GetContentType method [Open Packaging Conventions]","GetContentType method [Open Packaging Conventions]","IOpcPart interface","IOpcPart interface [Open Packaging Conventions]","GetContentType method","IOpcPart.GetContentType","IOpcPart::GetContentType","msopc/IOpcPart::GetContentType","opc.iopcpart_getcontenttype"]
old-location: opc\iopcpart_getcontenttype.htm
tech.root: OPC
ms.assetid: fe0d6ba3-8c62-4269-86ff-669609529933
ms.date: 12/05/2018
ms.keywords: GetContentType, GetContentType method [Open Packaging Conventions], GetContentType method [Open Packaging Conventions],IOpcPart interface, IOpcPart interface [Open Packaging Conventions],GetContentType method, IOpcPart.GetContentType, IOpcPart::GetContentType, msopc/IOpcPart::GetContentType, opc.iopcpart_getcontenttype
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
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
 - IOpcPart::GetContentType
 - msopc/IOpcPart::GetContentType
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
 - IOpcPart.GetContentType
---

# IOpcPart::GetContentType


## -description

Gets the media  type of part content.

## -parameters

### -param contentType [out, retval]

The media  type of part content, as specified by the package format designer and adhering to <a href="https://www.w3.org/Protocols/rfc2616/rfc2616.html">RFC 2616: HTTP/1.1</a>.

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
The <i>contentType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>contentType</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

For more information about parts, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="https://www.w3.org/Protocols/rfc2616/rfc2616.html">RFC 2616: HTTP/1.1</a>



<b>Reference</b>