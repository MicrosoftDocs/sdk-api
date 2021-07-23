---
UID: NF:appxpackaging.IAppxFile.GetCompressionOption
title: IAppxFile::GetCompressionOption (appxpackaging.h)
description: Retrieves the compression option that is used to store the file in the package.
helpviewer_keywords: ["GetCompressionOption","GetCompressionOption method [App packaging and management]","GetCompressionOption method [App packaging and management]","IAppxFile interface","IAppxFile interface [App packaging and management]","GetCompressionOption method","IAppxFile.GetCompressionOption","IAppxFile::GetCompressionOption","appxpackaging/IAppxFile::GetCompressionOption","appxpkg.iappxfile_getcompressionoption"]
old-location: appxpkg\iappxfile_getcompressionoption.htm
tech.root: appxpkg
ms.assetid: E2F33ED4-EAD3-44AE-B646-3AB875FA7606
ms.date: 12/05/2018
ms.keywords: GetCompressionOption, GetCompressionOption method [App packaging and management], GetCompressionOption method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetCompressionOption method, IAppxFile.GetCompressionOption, IAppxFile::GetCompressionOption, appxpackaging/IAppxFile::GetCompressionOption, appxpkg.iappxfile_getcompressionoption
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
 - IAppxFile::GetCompressionOption
 - appxpackaging/IAppxFile::GetCompressionOption
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
 - IAppxFile.GetCompressionOption
---

# IAppxFile::GetCompressionOption


## -description

Retrieves the compression option that is used to store the file in the package.

## -parameters

### -param compressionOption [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_compression_option">APPX_COMPRESSION_OPTION</a>*</b>

A compression option that describes how the file is stored in the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_compression_option">APPX_COMPRESSION_OPTION</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>