---
UID: NF:appxpackaging.IAppxFile.GetCompressionOption
title: IAppxFile::GetCompressionOption (appxpackaging.h)
author: windows-sdk-content
description: Retrieves the compression option that is used to store the file in the package.
old-location: appxpkg\iappxfile_getcompressionoption.htm
tech.root: appxpkg
ms.assetid: E2F33ED4-EAD3-44AE-B646-3AB875FA7606
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCompressionOption, GetCompressionOption method [App packaging and management], GetCompressionOption method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetCompressionOption method, IAppxFile.GetCompressionOption, IAppxFile::GetCompressionOption, appxpackaging/IAppxFile::GetCompressionOption, appxpkg.iappxfile_getcompressionoption
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFile.GetCompressionOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFile::GetCompressionOption


## -description


Retrieves the compression option that is used to store the file in the package.


## -parameters




### -param compressionOption [out, retval]

Type: <b><a href="https://msdn.microsoft.com/C4FEE4DA-1097-4870-BB43-A910E20BCBD6">APPX_COMPRESSION_OPTION</a>*</b>

A compression option that describes how the file is stored in the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C4FEE4DA-1097-4870-BB43-A910E20BCBD6">APPX_COMPRESSION_OPTION</a>



<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>
 

 

