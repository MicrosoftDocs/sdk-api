---
UID: NF:appxpackaging.IAppxPackageWriter.Close
title: IAppxPackageWriter::Close (appxpackaging.h)
description: Writes footprint files at the end of the app package, and closes the package writer object's output stream.
helpviewer_keywords: ["Close","Close method [App packaging and management]","Close method [App packaging and management]","IAppxPackageWriter interface","IAppxPackageWriter interface [App packaging and management]","Close method","IAppxPackageWriter.Close","IAppxPackageWriter::Close","appxpackaging/IAppxPackageWriter::Close","appxpkg.iappxpackagewriter_close"]
old-location: appxpkg\iappxpackagewriter_close.htm
tech.root: appxpkg
ms.assetid: 294625B2-1141-44EE-A769-365C3B37EBD9
ms.date: 12/05/2018
ms.keywords: Close, Close method [App packaging and management], Close method [App packaging and management],IAppxPackageWriter interface, IAppxPackageWriter interface [App packaging and management],Close method, IAppxPackageWriter.Close, IAppxPackageWriter::Close, appxpackaging/IAppxPackageWriter::Close, appxpkg.iappxpackagewriter_close
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
 - IAppxPackageWriter::Close
 - appxpackaging/IAppxPackageWriter::Close
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
 - IAppxPackageWriter.Close
---

# IAppxPackageWriter::Close


## -description

Writes footprint files at the end of the app package, and closes the package writer object's output stream.

## -parameters

### -param manifest [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream that provides the contents of the manifest for the package. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.

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
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The input stream contains a manifest that is not valid. 

</td>
</tr>
</table>

## -remarks

The <b>Close</b> method should be called only after all payload files have been added to the package. 


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-create-a-package">How to create an app  package</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a>