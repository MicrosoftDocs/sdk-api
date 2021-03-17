---
UID: NF:appxpackaging.IAppxBundleFactory.CreateBundleReader
title: IAppxBundleFactory::CreateBundleReader (appxpackaging.h)
description: Creates a read-only bundle object that reads its contents from an IStream object.
helpviewer_keywords: ["CreateBundleReader","CreateBundleReader method [App packaging and management]","CreateBundleReader method [App packaging and management]","IAppxBundleFactory interface","IAppxBundleFactory interface [App packaging and management]","CreateBundleReader method","IAppxBundleFactory.CreateBundleReader","IAppxBundleFactory::CreateBundleReader","appxpackaging/IAppxBundleFactory::CreateBundleReader","appxpkg.iappxbundlefactory_createbundlereader"]
old-location: appxpkg\iappxbundlefactory_createbundlereader.htm
tech.root: appxpkg
ms.assetid: 3D9F7A0A-EF6A-4C99-B9A0-C618138DB5ED
ms.date: 12/05/2018
ms.keywords: CreateBundleReader, CreateBundleReader method [App packaging and management], CreateBundleReader method [App packaging and management],IAppxBundleFactory interface, IAppxBundleFactory interface [App packaging and management],CreateBundleReader method, IAppxBundleFactory.CreateBundleReader, IAppxBundleFactory::CreateBundleReader, appxpackaging/IAppxBundleFactory::CreateBundleReader, appxpkg.iappxbundlefactory_createbundlereader
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleFactory::CreateBundleReader
 - appxpackaging/IAppxBundleFactory::CreateBundleReader
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
 - IAppxBundleFactory.CreateBundleReader
---

# IAppxBundleFactory::CreateBundleReader


## -description

Creates a read-only bundle object that reads its contents from an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.

## -parameters

### -param inputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The input stream that delivers the content of the package for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param bundleReader [out, retval]

Type: <b>IAppxBundleReader**</b>

A  bundle  reader.

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
The bundle manifest is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a>