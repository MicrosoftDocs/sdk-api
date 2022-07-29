---
UID: NF:appxpackaging.IAppxBundleWriter.AddPayloadPackage
title: IAppxBundleWriter::AddPayloadPackage (appxpackaging.h)
description: Adds a new app package to the bundle. (IAppxBundleWriter.AddPayloadPackage)
helpviewer_keywords: ["AddPayloadPackage","AddPayloadPackage method [App packaging and management]","AddPayloadPackage method [App packaging and management]","IAppxBundleWriter interface","IAppxBundleWriter interface [App packaging and management]","AddPayloadPackage method","IAppxBundleWriter.AddPayloadPackage","IAppxBundleWriter::AddPayloadPackage","appxpackaging/IAppxBundleWriter::AddPayloadPackage","appxpkg.iappxbundlewriter_addpayloadpackage"]
old-location: appxpkg\iappxbundlewriter_addpayloadpackage.htm
tech.root: appxpkg
ms.assetid: 4772621D-2A8E-439B-8AD7-01A5BD31002B
ms.date: 12/05/2018
ms.keywords: AddPayloadPackage, AddPayloadPackage method [App packaging and management], AddPayloadPackage method [App packaging and management],IAppxBundleWriter interface, IAppxBundleWriter interface [App packaging and management],AddPayloadPackage method, IAppxBundleWriter.AddPayloadPackage, IAppxBundleWriter::AddPayloadPackage, appxpackaging/IAppxBundleWriter::AddPayloadPackage, appxpkg.iappxbundlewriter_addpayloadpackage
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
 - IAppxBundleWriter::AddPayloadPackage
 - appxpackaging/IAppxBundleWriter::AddPayloadPackage
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
 - IAppxBundleWriter.AddPayloadPackage
---

# IAppxBundleWriter::AddPayloadPackage


## -description

Adds a new app package to the bundle.

## -parameters

### -param fileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the payload file. The file name path must be relative to the root of the package.

### -param packageStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of <i>fileName</i>.
          The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. Error OPC codes, in addition to  OPC_E_DUPLICATE_PART may result. If the method fails, the bundle writer will close in a failed state and can't be used any more.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The file name specified is already in use in the bundle. 

</td>
</tr>
</table>

## -remarks

When the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile">AddPayloadFile</a> method succeeds the contents of the specified <i>fileName</i> are written to the package and a corresponding entry is made in the package block map.

<b>AddPayloadPackage</b> reads the content of the app package from <i>packageStream</i> and stores the content in the bundle with the given <i>fileName</i>. 

<b>AddPayloadPackage</b> can fail if:

<ul>
<li><i>packageStream</i> doesn't deliver a valid app package</li>
<li>The app package delivered by <i>packageStream</i> is in a different package family than an app package already added to the bundle</li>
<li>The app package delivered by <i>packageStream</i> is targeted to an architecture that can't reside in the same bundle as another app package already added to the bundle</li>
<li>The app package delivered by <i>packageStream</i> has a block map that uses a different hash method than an app package already added to the bundle</li>
<li><i>fileName</i> isn't a valid file name, is a reserved name, or is already used by another app package added to the bundle</li>
</ul>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter">IAppxBundleWriter</a>
