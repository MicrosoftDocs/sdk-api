---
UID: NF:appxpackaging.IAppxFactory.CreatePackageReader
title: IAppxFactory::CreatePackageReader (appxpackaging.h)
description: Creates a read-only package reader from the contents provided by an IStream. This method does not validate the digital signature.
helpviewer_keywords: ["CreatePackageReader","CreatePackageReader method [App packaging and management]","CreatePackageReader method [App packaging and management]","IAppxFactory interface","IAppxFactory interface [App packaging and management]","CreatePackageReader method","IAppxFactory.CreatePackageReader","IAppxFactory::CreatePackageReader","appxpackaging/IAppxFactory::CreatePackageReader","appxpkg.iappxfactory_createpackagereader"]
old-location: appxpkg\iappxfactory_createpackagereader.htm
tech.root: appxpkg
ms.assetid: 60C9781F-A1EE-4EAA-9CD5-32692F3E063D
ms.date: 12/05/2018
ms.keywords: CreatePackageReader, CreatePackageReader method [App packaging and management], CreatePackageReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreatePackageReader method, IAppxFactory.CreatePackageReader, IAppxFactory::CreatePackageReader, appxpackaging/IAppxFactory::CreatePackageReader, appxpkg.iappxfactory_createpackagereader
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
 - IAppxFactory::CreatePackageReader
 - appxpackaging/IAppxFactory::CreatePackageReader
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
 - IAppxFactory.CreatePackageReader
---

# IAppxFactory::CreatePackageReader


## -description

Creates a read-only package reader from the contents provided by an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. This method does not validate the <a href="/previous-versions/windows/hh464986(v=win.10)">digital signature</a>.

## -parameters

### -param inputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The input stream that delivers the content of the package for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param packageReader [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>**</b>

A  package  reader.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INTERLEAVING_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
The ZIP file delivered by <i>inputStream</i> is an interleaved OPC package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_RELATIONSHIPS_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
The OPC package delivered by <i>inputStream</i> contains OPC package/part relationships.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_MISSING_REQUIRED_FILE</b></dt>
</dl>
</td>
<td width="60%">
The OPC package delivered by <i>inputStream</i> does not have a manifest, or a block map, or a signature file when a CI catalog is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The package manifest is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_BLOCKMAP</b></dt>
</dl>
</td>
<td width="60%">
The package block map is not valid, the list of files in the ZIP central directory does not match the list of files in the block map, or the size of files listed in the ZIP central directory does not match the file and block sizes listed in the block map.

</td>
</tr>
</table>

## -remarks

The  <b>CreatePackageReader</b> method immediately retrieves footprint elements of the app package through the stream and validates their content.  This method succeeds only if the OPC package and all footprint elements (including ZIP central directory, manifest, [Content_Types].xml, and block map) are valid.  


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-extract-content-from-a-package">Quickstart: Extract app package contents</a> and <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>