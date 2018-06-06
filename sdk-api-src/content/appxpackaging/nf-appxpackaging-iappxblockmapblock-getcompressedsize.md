---
UID: NF:appxpackaging.IAppxBlockMapBlock.GetCompressedSize
title: IAppxBlockMapBlock::GetCompressedSize
author: windows-sdk-content
description: Retrieves compressed size of the block.
old-location: appxpkg\iappxblockmapblock_getcompressedsize.htm
old-project: appxpkg
ms.assetid: 02B5F96E-EA8B-407F-98D8-BF6BFF72B346
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetCompressedSize, GetCompressedSize method [App packaging and management], GetCompressedSize method [App packaging and management],IAppxBlockMapBlock interface, IAppxBlockMapBlock interface [App packaging and management],GetCompressedSize method, IAppxBlockMapBlock.GetCompressedSize, IAppxBlockMapBlock::GetCompressedSize, appxpackaging/IAppxBlockMapBlock::GetCompressedSize, appxpkg.iappxblockmapblock_getcompressedsize
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxBlockMapBlock.GetCompressedSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapBlock::GetCompressedSize


## -description


Retrieves compressed size of the block.


## -parameters




### -param size [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a>*</b>

The compressed size of the block, in bytes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This size corresponds to the compressed size of the block. 

The <i>size</i> value corresponds to the <b>Size</b> attribute of the <a href="https://msdn.microsoft.com/7b4a9f58-a370-41f1-9234-004fc8ba425b">Block</a> element in the block map.




## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>
 

 

