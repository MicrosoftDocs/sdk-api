---
UID: NF:msopc.IOpcPart.GetContentStream
title: IOpcPart::GetContentStream (msopc.h)
description: Gets a stream that provides read/write access to part content.
helpviewer_keywords: ["GetContentStream","GetContentStream method [Open Packaging Conventions]","GetContentStream method [Open Packaging Conventions]","IOpcPart interface","IOpcPart interface [Open Packaging Conventions]","GetContentStream method","IOpcPart.GetContentStream","IOpcPart::GetContentStream","msopc/IOpcPart::GetContentStream","opc.iopcpart_getcontentstream"]
old-location: opc\iopcpart_getcontentstream.htm
tech.root: OPC
ms.assetid: b40e3df2-e717-465d-8893-511e4776d80d
ms.date: 12/05/2018
ms.keywords: GetContentStream, GetContentStream method [Open Packaging Conventions], GetContentStream method [Open Packaging Conventions],IOpcPart interface, IOpcPart interface [Open Packaging Conventions],GetContentStream method, IOpcPart.GetContentStream, IOpcPart::GetContentStream, msopc/IOpcPart::GetContentStream, opc.iopcpart_getcontentstream
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
 - IOpcPart::GetContentStream
 - msopc/IOpcPart::GetContentStream
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
 - IOpcPart.GetContentStream
---

# IOpcPart::GetContentStream


## -description

Gets a stream that provides read/write access to  part content.

## -parameters

### -param stream [out, retval]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of a stream that provides read and write access to part content.

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
The <i>stream</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CreateFile function error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function, which is returned as a result of attempting to allocate disk space for part data if the 
    package was opened using the <b>OPC_CACHE_ON_ACCESS</b> read flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/package-consumption-error-group">Package Consumption Error Group</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/part-uri-error-group">Part URI Error Group</a>. 

</td>
</tr>
</table>

## -remarks

For more information about parts, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>