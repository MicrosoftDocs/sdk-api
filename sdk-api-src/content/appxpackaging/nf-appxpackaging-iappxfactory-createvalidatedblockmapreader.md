---
UID: NF:appxpackaging.IAppxFactory.CreateValidatedBlockMapReader
title: IAppxFactory::CreateValidatedBlockMapReader (appxpackaging.h)
description: Creates a read-only block map object model from contents provided by an IStream and a digital signature.
helpviewer_keywords: ["CreateValidatedBlockMapReader","CreateValidatedBlockMapReader method [App packaging and management]","CreateValidatedBlockMapReader method [App packaging and management]","IAppxFactory interface","IAppxFactory interface [App packaging and management]","CreateValidatedBlockMapReader method","IAppxFactory.CreateValidatedBlockMapReader","IAppxFactory::CreateValidatedBlockMapReader","appxpackaging/IAppxFactory::CreateValidatedBlockMapReader","appxpkg.iappxfactory_createvalidatedblockmapreader"]
old-location: appxpkg\iappxfactory_createvalidatedblockmapreader.htm
tech.root: appxpkg
ms.assetid: BCC39D9C-4AF9-4CFD-AC66-4B79F9F25BDC
ms.date: 12/05/2018
ms.keywords: CreateValidatedBlockMapReader, CreateValidatedBlockMapReader method [App packaging and management], CreateValidatedBlockMapReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateValidatedBlockMapReader method, IAppxFactory.CreateValidatedBlockMapReader, IAppxFactory::CreateValidatedBlockMapReader, appxpackaging/IAppxFactory::CreateValidatedBlockMapReader, appxpkg.iappxfactory_createvalidatedblockmapreader
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
 - IAppxFactory::CreateValidatedBlockMapReader
 - appxpackaging/IAppxFactory::CreateValidatedBlockMapReader
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
 - IAppxFactory.CreateValidatedBlockMapReader
---

# IAppxFactory::CreateValidatedBlockMapReader


## -description

Creates a read-only block map object model from contents provided by an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> and a digital signature.

## -parameters

### -param blockMapStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream that delivers block map XML for reading. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.

### -param signatureFileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The file that contains a digital signature used to validate the contents of the input stream.

### -param blockMapReader [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>**</b>

The block map reader.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those below. This method might return errors that are passed from the underlying validation APIs that are used.
For example, this method might return "Crypto and WinTrust error codes (0x8009xxxx, 0x800bxxxx) if the signature can't be read, is invalid, or doesn't match the content of <i>blockMapStream</i>.


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
The <i>blockMapStream</i> does not contain syntactically valid XML for the block map.

</td>
</tr>
</table>

## -remarks

This method is used when the block map exists alone, outside of an app package.  The block map object provides access to all data elements and attributes in the block map XML.

The <i>fileName</i> parameter should include the path of a package digital signature (.p7x) file on disk.  If this parameter is not <b>NULL</b>, this method will validate the format of the signature file and validate the contents of <i>blockMapStream</i> against the signature.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createblockmapreader">IAppxFactory::CreateBlockMapReader</a>