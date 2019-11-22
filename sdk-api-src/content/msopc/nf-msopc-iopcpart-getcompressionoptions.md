---
UID: NF:msopc.IOpcPart.GetCompressionOptions
title: IOpcPart::GetCompressionOptions (msopc.h)

description: Gets a value that describes the way part content is compressed.
old-location: opc\iopcpart_getcompressionoptions.htm
tech.root: OPC
ms.assetid: aee8e3a2-3fac-40da-bea2-1fd4e2224c81

ms.date: 12/05/2018
ms.keywords: GetCompressionOptions, GetCompressionOptions method [Open Packaging Conventions], GetCompressionOptions method [Open Packaging Conventions],IOpcPart interface, IOpcPart interface [Open Packaging Conventions],GetCompressionOptions method, IOpcPart.GetCompressionOptions, IOpcPart::GetCompressionOptions, msopc/IOpcPart::GetCompressionOptions, opc.iopcpart_getcompressionoptions
ms.topic: method
f1_keywords: 
 - "msopc/IOpcPart.GetCompressionOptions"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcPart.GetCompressionOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcPart::GetCompressionOptions


## -description


Gets a value that describes the way part content is compressed.


## -parameters




### -param compressionOptions [out, retval]

A value that describes the way part content is compressed.


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
The <i>compressionOptions</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information about parts, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_compression_options">OPC_COMPRESSION_OPTIONS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>
 

 

