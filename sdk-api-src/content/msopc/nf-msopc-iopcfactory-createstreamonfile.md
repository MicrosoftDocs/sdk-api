---
UID: NF:msopc.IOpcFactory.CreateStreamOnFile
title: IOpcFactory::CreateStreamOnFile (msopc.h)
description: Creates a stream over a file.
helpviewer_keywords: ["CreateStreamOnFile","CreateStreamOnFile method [Open Packaging Conventions]","CreateStreamOnFile method [Open Packaging Conventions]","IOpcFactory interface","IOpcFactory interface [Open Packaging Conventions]","CreateStreamOnFile method","IOpcFactory.CreateStreamOnFile","IOpcFactory::CreateStreamOnFile","msopc/IOpcFactory::CreateStreamOnFile","opc.iopcfactory_createstreamonfile"]
old-location: opc\iopcfactory_createstreamonfile.htm
tech.root: OPC
ms.assetid: d41bb51d-127c-4b24-8c93-4224404e0b2d
ms.date: 12/05/2018
ms.keywords: CreateStreamOnFile, CreateStreamOnFile method [Open Packaging Conventions], CreateStreamOnFile method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreateStreamOnFile method, IOpcFactory.CreateStreamOnFile, IOpcFactory::CreateStreamOnFile, msopc/IOpcFactory::CreateStreamOnFile, opc.iopcfactory_createstreamonfile
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcFactory::CreateStreamOnFile
 - msopc/IOpcFactory::CreateStreamOnFile
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
 - IOpcFactory.CreateStreamOnFile
---

# IOpcFactory::CreateStreamOnFile


## -description

Creates a stream over a file. This method is a simplified wrapper for a call to the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. <b>CreateFile</b> parameters that are not exposed through this method use their default values. For more information, see <b>CreateFile</b>.

## -parameters

### -param filename [in]

The name of the file over which the stream is created.

### -param ioMode [in]

The value that describes the read/write status of the stream to be created.

### -param securityAttributes [in]

For information about the <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure in this parameter, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwFlagsAndAttributes [in]

The settings and attributes of the file. For most files, <b>FILE_ATTRIBUTE_NORMAL</b> can be used.

For more information about this parameter, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param stream [out, retval]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the stream.

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
The value passed in the <i>ioMode</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_stream_io_mode">OPC_STREAM_IO_MODE</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>filename</i> and <i>stream</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CreateFile</b> function error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. 

</td>
</tr>
</table>

## -remarks

Do not use a stream to serialize package data when the same stream is being used to deserialize a package, because the attempt may result in undefined behavior.

For information about using this method when loading or saving a package, see the <a href="/previous-versions/windows/desktop/opc/loading-a-package">Loading a Package</a> or  <a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a> programming task. 

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>, and <a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/previous-versions/windows/desktop/opc/loading-a-package">Loading a Package</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_stream_io_mode">OPC_STREAM_IO_MODE</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="/windows/desktop/win7ip/platform-update-for-windows-vista-portal">Platform Update for Windows Vista</a>



<a href="https://www.ietf.org/rfc/rfc3986.txt">RFC 3986: URI Generic Syntax</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a>