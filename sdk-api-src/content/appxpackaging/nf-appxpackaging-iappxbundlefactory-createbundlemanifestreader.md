---
UID: NF:appxpackaging.IAppxBundleFactory.CreateBundleManifestReader
title: IAppxBundleFactory::CreateBundleManifestReader (appxpackaging.h)
description: Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.
helpviewer_keywords: ["CreateBundleManifestReader","CreateBundleManifestReader method [App packaging and management]","CreateBundleManifestReader method [App packaging and management]","IAppxBundleFactory interface","IAppxBundleFactory interface [App packaging and management]","CreateBundleManifestReader method","IAppxBundleFactory.CreateBundleManifestReader","IAppxBundleFactory::CreateBundleManifestReader","appxpackaging/IAppxBundleFactory::CreateBundleManifestReader","appxpkg.iappxbundlefactory_createbundlemanifestreader"]
old-location: appxpkg\iappxbundlefactory_createbundlemanifestreader.htm
tech.root: appxpkg
ms.assetid: 8D537830-A8AA-4652-B6F2-F7A545B8877E
ms.date: 12/05/2018
ms.keywords: CreateBundleManifestReader, CreateBundleManifestReader method [App packaging and management], CreateBundleManifestReader method [App packaging and management],IAppxBundleFactory interface, IAppxBundleFactory interface [App packaging and management],CreateBundleManifestReader method, IAppxBundleFactory.CreateBundleManifestReader, IAppxBundleFactory::CreateBundleManifestReader, appxpackaging/IAppxBundleFactory::CreateBundleManifestReader, appxpkg.iappxbundlefactory_createbundlemanifestreader
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
 - IAppxBundleFactory::CreateBundleManifestReader
 - appxpackaging/IAppxBundleFactory::CreateBundleManifestReader
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
 - IAppxBundleFactory.CreateBundleManifestReader
---

# IAppxBundleFactory::CreateBundleManifestReader


## -description

Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.

## -parameters

### -param inputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The input stream  that delivers the manifest XML for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param manifestReader [out, retval]

Type: <b>IAppxBundleManifestReader**</b>

The manifest reader.

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
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>inputStream</i> does not contain syntactically valid XML for the manifest.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a>