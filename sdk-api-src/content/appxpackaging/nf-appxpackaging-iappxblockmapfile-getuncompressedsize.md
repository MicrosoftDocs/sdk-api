---
UID: NF:appxpackaging.IAppxBlockMapFile.GetUncompressedSize
title: IAppxBlockMapFile::GetUncompressedSize
author: windows-sdk-content
description: Retrieves the uncompressed size of the associated zip file item.
old-location: appxpkg\iappxblockmapfile_getuncompressedsize.htm
tech.root: appxpkg
ms.assetid: 35D3EADC-F8EF-4D8F-8016-2E30976965EC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUncompressedSize, GetUncompressedSize method [App packaging and management], GetUncompressedSize method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetUncompressedSize method, IAppxBlockMapFile.GetUncompressedSize, IAppxBlockMapFile::GetUncompressedSize, appxpackaging/IAppxBlockMapFile::GetUncompressedSize, appxpkg.iappxblockmapfile_getuncompressedsize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxBlockMapFile.GetUncompressedSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBlockMapFile::GetUncompressedSize


## -description


Retrieves the uncompressed size of the associated zip file item.


## -parameters




### -param size [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

 In a valid app package, <i>size</i> is the uncompressed size of the associated zip file item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

