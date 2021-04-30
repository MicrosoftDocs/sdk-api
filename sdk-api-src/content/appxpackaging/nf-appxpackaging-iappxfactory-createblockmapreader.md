---
UID: NF:appxpackaging.IAppxFactory.CreateBlockMapReader
title: IAppxFactory::CreateBlockMapReader (appxpackaging.h)
description: Creates a read-only block map object model from contents provided by an IStream.
helpviewer_keywords: ["CreateBlockMapReader","CreateBlockMapReader method [App packaging and management]","CreateBlockMapReader method [App packaging and management]","IAppxFactory interface","IAppxFactory interface [App packaging and management]","CreateBlockMapReader method","IAppxFactory.CreateBlockMapReader","IAppxFactory::CreateBlockMapReader","appxpackaging/IAppxFactory::CreateBlockMapReader","appxpkg.iappxfactory_createblockmapreader"]
old-location: appxpkg\iappxfactory_createblockmapreader.htm
tech.root: appxpkg
ms.assetid: B4A310F0-4276-49AA-9ABF-A98F41E8F87F
ms.date: 12/05/2018
ms.keywords: CreateBlockMapReader, CreateBlockMapReader method [App packaging and management], CreateBlockMapReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateBlockMapReader method, IAppxFactory.CreateBlockMapReader, IAppxFactory::CreateBlockMapReader, appxpackaging/IAppxFactory::CreateBlockMapReader, appxpkg.iappxfactory_createblockmapreader
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
 - IAppxFactory::CreateBlockMapReader
 - appxpackaging/IAppxFactory::CreateBlockMapReader
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
 - IAppxFactory.CreateBlockMapReader
---

# IAppxFactory::CreateBlockMapReader


## -description

Creates a read-only block map object model from contents provided by an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -parameters

### -param inputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream that delivers the block map XML for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param blockMapReader [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>**</b>

The block map reader.

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
<dt><b>APPX_E_INVALID_BLOCKMAP</b></dt>
</dl>
</td>
<td width="60%">
The <i>inputStream</i> does not contain syntactically valid XML for the block map.

</td>
</tr>
</table>

## -remarks

Use the  <b>CreateBlockMapReader</b> method to read a block map outside of an app package.  The <i>blockMapReader</i> provides access to all data elements and attributes in the block map XML.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createvalidatedblockmapreader">IAppxFactory::CreateValidatedBlockMapReader</a>