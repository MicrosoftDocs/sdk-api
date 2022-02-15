---
UID: NF:appxpackaging.IAppxBlockMapFile.GetUncompressedSize
title: IAppxBlockMapFile::GetUncompressedSize (appxpackaging.h)
description: Retrieves the uncompressed size of the associated zip file item.
helpviewer_keywords: ["GetUncompressedSize","GetUncompressedSize method [App packaging and management]","GetUncompressedSize method [App packaging and management]","IAppxBlockMapFile interface","IAppxBlockMapFile interface [App packaging and management]","GetUncompressedSize method","IAppxBlockMapFile.GetUncompressedSize","IAppxBlockMapFile::GetUncompressedSize","appxpackaging/IAppxBlockMapFile::GetUncompressedSize","appxpkg.iappxblockmapfile_getuncompressedsize"]
old-location: appxpkg\iappxblockmapfile_getuncompressedsize.htm
tech.root: appxpkg
ms.assetid: 35D3EADC-F8EF-4D8F-8016-2E30976965EC
ms.date: 12/05/2018
ms.keywords: GetUncompressedSize, GetUncompressedSize method [App packaging and management], GetUncompressedSize method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetUncompressedSize method, IAppxBlockMapFile.GetUncompressedSize, IAppxBlockMapFile::GetUncompressedSize, appxpackaging/IAppxBlockMapFile::GetUncompressedSize, appxpkg.iappxblockmapfile_getuncompressedsize
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
 - IAppxBlockMapFile::GetUncompressedSize
 - appxpackaging/IAppxBlockMapFile::GetUncompressedSize
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
 - IAppxBlockMapFile.GetUncompressedSize
---

# IAppxBlockMapFile::GetUncompressedSize


## -description

Retrieves the uncompressed size of the associated zip file item.

## -parameters

### -param size [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>*</b>

 In a valid app package, <i>size</i> is the uncompressed size of the associated zip file item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>