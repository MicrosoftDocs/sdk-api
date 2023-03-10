---
UID: NF:appxpackaging.IAppxBlockMapReader.GetFile
title: IAppxBlockMapReader::GetFile (appxpackaging.h)
description: Retrieves data corresponding to a file in the block map with the specified file name.
helpviewer_keywords: ["GetFile","GetFile method [App packaging and management]","GetFile method [App packaging and management]","IAppxBlockMapReader interface","IAppxBlockMapReader interface [App packaging and management]","GetFile method","IAppxBlockMapReader.GetFile","IAppxBlockMapReader::GetFile","appxpackaging/IAppxBlockMapReader::GetFile","appxpkg.iappxblockmapreader_getfile"]
old-location: appxpkg\iappxblockmapreader_getfile.htm
tech.root: appxpkg
ms.assetid: 3F38BC3A-9CFD-4FB3-A744-612E25DF0F0F
ms.date: 12/05/2018
ms.keywords: GetFile, GetFile method [App packaging and management], GetFile method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetFile method, IAppxBlockMapReader.GetFile, IAppxBlockMapReader::GetFile, appxpackaging/IAppxBlockMapReader::GetFile, appxpkg.iappxblockmapreader_getfile
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
 - IAppxBlockMapReader::GetFile
 - appxpackaging/IAppxBlockMapReader::GetFile
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
 - IAppxBlockMapReader.GetFile
---

# IAppxBlockMapReader::GetFile


## -description

Retrieves data corresponding to a file in the block map with the specified file name.

## -parameters

### -param filename [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the file.

### -param file [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>**</b>

The data about the file's attributes and blocks.

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
The specified file name does not match the name of a file listed in the block map.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>