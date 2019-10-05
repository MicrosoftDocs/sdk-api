---
UID: NF:appxpackaging.IAppxPackageReader.GetBlockMap
title: IAppxPackageReader::GetBlockMap (appxpackaging.h)
author: windows-sdk-content
description: Retrieves the block map object model of the package.
old-location: appxpkg\iappxpackagereader_getblockmap.htm
tech.root: appxpkg
ms.assetid: FEBCA2E4-9B32-499B-AD31-9D90525A42DB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBlockMap, GetBlockMap method [App packaging and management], GetBlockMap method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetBlockMap method, IAppxPackageReader.GetBlockMap, IAppxPackageReader::GetBlockMap, appxpackaging/IAppxPackageReader::GetBlockMap, appxpkg.iappxpackagereader_getblockmap
ms.topic: method
f1_keywords: 
 - "appxpackaging/IAppxPackageReader.GetBlockMap"
dev_langs:
 - c++
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
 - IAppxPackageReader.GetBlockMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxPackageReader::GetBlockMap


## -description


Retrieves the block map object model of the package.


## -parameters




### -param blockMapReader [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>**</b>

The object model of the block map of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The package block map is validated when the package reader is created using <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>
 

 

