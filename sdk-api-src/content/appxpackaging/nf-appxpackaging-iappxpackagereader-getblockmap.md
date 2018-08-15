---
UID: NF:appxpackaging.IAppxPackageReader.GetBlockMap
title: IAppxPackageReader::GetBlockMap
author: windows-sdk-content
description: Retrieves the block map object model of the package.
old-location: appxpkg\iappxpackagereader_getblockmap.htm
old-project: appxpkg
ms.assetid: FEBCA2E4-9B32-499B-AD31-9D90525A42DB
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetBlockMap, GetBlockMap method [App packaging and management], GetBlockMap method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetBlockMap method, IAppxPackageReader.GetBlockMap, IAppxPackageReader::GetBlockMap, appxpackaging/IAppxPackageReader::GetBlockMap, appxpkg.iappxpackagereader_getblockmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageReader.GetBlockMap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageReader::GetBlockMap


## -description


Retrieves the block map object model of the package.


## -parameters




### -param blockMapReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>**</b>

The object model of the block map of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The package block map is validated when the package reader is created using <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>.




## -see-also




<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>
 

 

