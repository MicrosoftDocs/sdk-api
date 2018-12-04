---
UID: NF:appxpackaging.IAppxBundleReader.GetBlockMap
title: IAppxBundleReader::GetBlockMap
author: windows-sdk-content
description: Retrieves a read-only block map object from the bundle.
old-location: appxpkg\iappxbundlereader_getblockmap.htm
tech.root: appxpkg
ms.assetid: 721940C7-0680-4AD0-93BC-20D630EDE228
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetBlockMap, GetBlockMap method [App packaging and management], GetBlockMap method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetBlockMap method, IAppxBundleReader.GetBlockMap, IAppxBundleReader::GetBlockMap, appxpackaging/IAppxBundleReader::GetBlockMap, appxpkg.iappxbundlereader_getblockmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleReader.GetBlockMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleReader::GetBlockMap


## -description


Retrieves a read-only block map object from the bundle.


## -parameters




### -param blockMapReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>**</b>

The object model of the block map of a package in the bundle.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

