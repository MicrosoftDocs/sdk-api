---
UID: NF:appxpackaging.IAppxPackageReader.GetFootprintFile
title: IAppxPackageReader::GetFootprintFile (appxpackaging.h)
description: Retrieves a footprint file from the package.
helpviewer_keywords: ["GetFootprintFile","GetFootprintFile method [App packaging and management]","GetFootprintFile method [App packaging and management]","IAppxPackageReader interface","IAppxPackageReader interface [App packaging and management]","GetFootprintFile method","IAppxPackageReader.GetFootprintFile","IAppxPackageReader::GetFootprintFile","appxpackaging/IAppxPackageReader::GetFootprintFile","appxpkg.iappxpackagereader_getfootprintfile"]
old-location: appxpkg\iappxpackagereader_getfootprintfile.htm
tech.root: appxpkg
ms.assetid: 8CCF9135-308F-4BDC-A67F-1E3ED2ACF565
ms.date: 12/05/2018
ms.keywords: GetFootprintFile, GetFootprintFile method [App packaging and management], GetFootprintFile method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetFootprintFile method, IAppxPackageReader.GetFootprintFile, IAppxPackageReader::GetFootprintFile, appxpackaging/IAppxPackageReader::GetFootprintFile, appxpkg.iappxpackagereader_getfootprintfile
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
 - IAppxPackageReader::GetFootprintFile
 - appxpackaging/IAppxPackageReader::GetFootprintFile
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
 - IAppxPackageReader.GetFootprintFile
---

# IAppxPackageReader::GetFootprintFile


## -description

Retrieves a footprint file from the package.

## -parameters

### -param type [in]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_footprint_file_type">APPX_FOOTPRINT_FILE_TYPE</a></b>

The type of footprint file to be retrieved.

### -param file [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>**</b>

The file object that corresponds to the footprint file of <i>type</i>.

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
The <i>type</i> parameter is not a member of the <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_footprint_file_type">APPX_FOOTPRINT_FILE_TYPE</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The package does not contain a footprint file of the specified type.


<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">GetFootprintFile</a> can return this error for <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_footprint_file_type">APPX_FOOTPRINT_FILE_TYPE_SIGNATURE</a> and <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_footprint_file_type">APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY</a> types.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfile">IAppxPackageReader::GetPayloadFile</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfiles">IAppxPackageReader::GetPayloadFiles</a>