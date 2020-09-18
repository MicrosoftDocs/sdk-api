---
UID: NF:appxpackaging.IAppxFactory.CreateManifestReader
title: IAppxFactory::CreateManifestReader (appxpackaging.h)
description: Creates a read-only manifest object model from contents provided by an IStream.
helpviewer_keywords: ["CreateManifestReader","CreateManifestReader method [App packaging and management]","CreateManifestReader method [App packaging and management]","IAppxFactory interface","IAppxFactory interface [App packaging and management]","CreateManifestReader method","IAppxFactory.CreateManifestReader","IAppxFactory::CreateManifestReader","appxpackaging/IAppxFactory::CreateManifestReader","appxpkg.iappxfactory_createmanifestreader"]
old-location: appxpkg\iappxfactory_createmanifestreader.htm
tech.root: appxpkg
ms.assetid: BF6C83FF-8CB1-47C0-84C3-E71059F0796E
ms.date: 12/05/2018
ms.keywords: CreateManifestReader, CreateManifestReader method [App packaging and management], CreateManifestReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateManifestReader method, IAppxFactory.CreateManifestReader, IAppxFactory::CreateManifestReader, appxpackaging/IAppxFactory::CreateManifestReader, appxpkg.iappxfactory_createmanifestreader
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
 - IAppxFactory::CreateManifestReader
 - appxpackaging/IAppxFactory::CreateManifestReader
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
 - IAppxFactory.CreateManifestReader
---

# IAppxFactory::CreateManifestReader


## -description

Creates a read-only manifest object model from contents provided by an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -parameters

### -param inputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The input stream  that delivers the manifest XML for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param manifestReader [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>**</b>

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

## -remarks

Use <b>CreateManifestReader</b> to read a manifest outside of an app package.  This method validates the manifest XML. The <i>manifestReader</i> provides access to all data elements and attributes in the manifest XML. The manifest logs the location of manifest validation errors in the ETW event log for AppxPackaging. 


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>