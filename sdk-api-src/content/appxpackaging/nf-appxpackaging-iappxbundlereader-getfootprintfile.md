---
UID: NF:appxpackaging.IAppxBundleReader.GetFootprintFile
title: IAppxBundleReader::GetFootprintFile (appxpackaging.h)
description: Retrieves the specified type of footprint file from the bundle.
helpviewer_keywords: ["GetFootprintFile","GetFootprintFile method [App packaging and management]","GetFootprintFile method [App packaging and management]","IAppxBundleReader interface","IAppxBundleReader interface [App packaging and management]","GetFootprintFile method","IAppxBundleReader.GetFootprintFile","IAppxBundleReader::GetFootprintFile","appxpackaging/IAppxBundleReader::GetFootprintFile","appxpkg.iappxbundlereader_getfootprintfile"]
old-location: appxpkg\iappxbundlereader_getfootprintfile.htm
tech.root: appxpkg
ms.assetid: BD60CD3E-2C08-4B97-B311-00C0EEBEF752
ms.date: 12/05/2018
ms.keywords: GetFootprintFile, GetFootprintFile method [App packaging and management], GetFootprintFile method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetFootprintFile method, IAppxBundleReader.GetFootprintFile, IAppxBundleReader::GetFootprintFile, appxpackaging/IAppxBundleReader::GetFootprintFile, appxpkg.iappxbundlereader_getfootprintfile
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
 - IAppxBundleReader::GetFootprintFile
 - appxpackaging/IAppxBundleReader::GetFootprintFile
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
 - IAppxBundleReader.GetFootprintFile
---

# IAppxBundleReader::GetFootprintFile


## -description

Retrieves the specified type of footprint file from the bundle.

## -parameters

### -param fileType [in]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_bundle_footprint_file_type">APPX_BUNDLE_FOOTPRINT_FILE_TYPE</a></b>

The type of footprint file to be retrieved.

### -param footprintFile [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>**</b>

The file object that corresponds to the footprint file of <i>fileType</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fileType</i> parameter is not a valid value in the <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_bundle_footprint_file_type">APPX_BUNDLE_FOOTPRINT_FILE_TYPE</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The bundle doesn't contain a footprint file of the specified type.


<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getfootprintfile">GetFootprintFile</a> can return this error for the <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_bundle_footprint_file_type">APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE</a> type.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlereader">IAppxBundleReader</a>