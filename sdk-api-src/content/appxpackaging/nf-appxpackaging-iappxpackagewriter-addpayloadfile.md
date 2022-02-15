---
UID: NF:appxpackaging.IAppxPackageWriter.AddPayloadFile
title: IAppxPackageWriter::AddPayloadFile (appxpackaging.h)
description: Adds a new payload file to the app package.
helpviewer_keywords: ["AddPayloadFile","AddPayloadFile method [App packaging and management]","AddPayloadFile method [App packaging and management]","IAppxPackageWriter interface","IAppxPackageWriter interface [App packaging and management]","AddPayloadFile method","IAppxPackageWriter.AddPayloadFile","IAppxPackageWriter::AddPayloadFile","appxpackaging/IAppxPackageWriter::AddPayloadFile","appxpkg.iappxpackagewriter_addpayloadfile"]
old-location: appxpkg\iappxpackagewriter_addpayloadfile.htm
tech.root: appxpkg
ms.assetid: 2BFC725A-CD56-46CA-983A-FD1BFB6CB474
ms.date: 12/05/2018
ms.keywords: AddPayloadFile, AddPayloadFile method [App packaging and management], AddPayloadFile method [App packaging and management],IAppxPackageWriter interface, IAppxPackageWriter interface [App packaging and management],AddPayloadFile method, IAppxPackageWriter.AddPayloadFile, IAppxPackageWriter::AddPayloadFile, appxpackaging/IAppxPackageWriter::AddPayloadFile, appxpkg.iappxpackagewriter_addpayloadfile
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - IAppxPackageWriter::AddPayloadFile
 - appxpackaging/IAppxPackageWriter::AddPayloadFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageWriter.AddPayloadFile
---

# IAppxPackageWriter::AddPayloadFile


## -description

Adds a new payload file to the app package.

## -parameters

### -param fileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the payload file. The file name path must be relative to the root of the package.

### -param contentType [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The string specifying the <a href="https://www.w3.org/Protocols/rfc2616/rfc2616.html">content type</a> of  <i>fileName</i>.

### -param compressionOption [in]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_compression_option">APPX_COMPRESSION_OPTION</a></b>

The type of compression to use  to store <i>fileName</i> in the package.

### -param inputStream [in]

Type: <b>IStream*</b>

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> providing the contents of <i>fileName</i>.
          The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. Error OPC codes, in addition to  OPC_E_DUPLICATE_PART may result. If the method fails, the package writer will close in a failed state and can't be used any more.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The compression option specified by <i>compressionOption</i> is not one of the values of the <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_compression_option">APPX_COMPRESSION_OPTION</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE </b></dt>
</dl>
</td>
<td width="60%">
The writer is closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_NAME)</b></dt>
</dl>
</td>
<td width="60%">
The file name specified is not a valid file name or is a reserved name for a footprint file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
</dl>
</td>
<td width="60%">
The file name specified is already in use in the package. 

</td>
</tr>
</table>

## -remarks

When the <b>AddPayloadFile</b> method succeeds the contents of the specified <i>fileName</i> are written to the package and a corresponding entry is made in the package block map.


<div class="alert"><b>Note</b>  Files with the following reserved filenames cannot be added to the package using the <b>AddPayloadFile</b> method:

`AppxManifest.xml`, `AppxBlockMap.xml`, `AppxStreamMap.xml`, and `AppxSignature.p7x`.

Also, files with the following reserved folder prefixes cannot be added to the package using the <b>AddPayloadFile</b> method: `\AppxMetadata\` and `\Microsoft.System.Package.Metadata\`. 





#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-create-a-package">How to create an app  package</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_compression_option">APPX_COMPRESSION_OPTION</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a>