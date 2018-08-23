---
UID: NF:appxpackaging.IAppxBlockMapFile.GetBlocks
title: IAppxBlockMapFile::GetBlocks
author: windows-sdk-content
description: Retrieves an enumerator for traversing the blocks of a file listed in the block map.
old-location: appxpkg\iappxblockmapfile_getblocks.htm
old-project: appxpkg
ms.assetid: CE8FB813-B125-4FD6-A7C3-CA3ECA72ECE7
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetBlocks, GetBlocks method [App packaging and management], GetBlocks method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetBlocks method, IAppxBlockMapFile.GetBlocks, IAppxBlockMapFile::GetBlocks, appxpackaging/IAppxBlockMapFile::GetBlocks, appxpkg.iappxblockmapfile_getblocks
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
 - IAppxBlockMapFile.GetBlocks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFile::GetBlocks


## -description


Retrieves an enumerator for traversing the blocks of a file listed in the block map.


## -parameters




### -param blocks [out, retval]

Type: <b><a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>**</b>

The enumerator for traversing the blocks. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

