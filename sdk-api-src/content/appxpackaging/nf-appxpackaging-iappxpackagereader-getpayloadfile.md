---
UID: NF:appxpackaging.IAppxPackageReader.GetPayloadFile
title: IAppxPackageReader::GetPayloadFile (appxpackaging.h)
description: Retrieves a payload file from the package.
helpviewer_keywords: ["GetPayloadFile","GetPayloadFile method [App packaging and management]","GetPayloadFile method [App packaging and management]","IAppxPackageReader interface","IAppxPackageReader interface [App packaging and management]","GetPayloadFile method","IAppxPackageReader.GetPayloadFile","IAppxPackageReader::GetPayloadFile","appxpackaging/IAppxPackageReader::GetPayloadFile","appxpkg.iappxpackagereader_getpayloadfile"]
old-location: appxpkg\iappxpackagereader_getpayloadfile.htm
tech.root: appxpkg
ms.assetid: 83E6931D-405C-4A93-BE70-F505D484CB7F
ms.date: 12/05/2018
ms.keywords: GetPayloadFile, GetPayloadFile method [App packaging and management], GetPayloadFile method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetPayloadFile method, IAppxPackageReader.GetPayloadFile, IAppxPackageReader::GetPayloadFile, appxpackaging/IAppxPackageReader::GetPayloadFile, appxpkg.iappxpackagereader_getpayloadfile
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
 - IAppxPackageReader::GetPayloadFile
 - appxpackaging/IAppxPackageReader::GetPayloadFile
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
 - IAppxPackageReader.GetPayloadFile
---

# IAppxPackageReader::GetPayloadFile


## -description

Retrieves a payload file from the package.

## -parameters

### -param fileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the payload file to be retrieved.

### -param file [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>**</b>

The file object that corresponds to <i>fileName</i>.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no payload file with the specified file name.

</td>
</tr>
</table>

## -remarks

The specified <i>fileName</i> must include the path relative to the package root directory.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">IAppxPackageReader::GetFootprintFile</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getpayloadfiles">IAppxPackageReader::GetPayloadFiles</a>