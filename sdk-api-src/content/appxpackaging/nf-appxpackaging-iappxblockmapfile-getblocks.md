---
UID: NF:appxpackaging.IAppxBlockMapFile.GetBlocks
title: IAppxBlockMapFile::GetBlocks (appxpackaging.h)
description: Retrieves an enumerator for traversing the blocks of a file listed in the block map.
helpviewer_keywords: ["GetBlocks","GetBlocks method [App packaging and management]","GetBlocks method [App packaging and management]","IAppxBlockMapFile interface","IAppxBlockMapFile interface [App packaging and management]","GetBlocks method","IAppxBlockMapFile.GetBlocks","IAppxBlockMapFile::GetBlocks","appxpackaging/IAppxBlockMapFile::GetBlocks","appxpkg.iappxblockmapfile_getblocks"]
old-location: appxpkg\iappxblockmapfile_getblocks.htm
tech.root: appxpkg
ms.assetid: CE8FB813-B125-4FD6-A7C3-CA3ECA72ECE7
ms.date: 12/05/2018
ms.keywords: GetBlocks, GetBlocks method [App packaging and management], GetBlocks method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetBlocks method, IAppxBlockMapFile.GetBlocks, IAppxBlockMapFile::GetBlocks, appxpackaging/IAppxBlockMapFile::GetBlocks, appxpkg.iappxblockmapfile_getblocks
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
 - IAppxBlockMapFile::GetBlocks
 - appxpackaging/IAppxBlockMapFile::GetBlocks
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
 - IAppxBlockMapFile.GetBlocks
---

# IAppxBlockMapFile::GetBlocks


## -description

Retrieves an enumerator for traversing the blocks of a file listed in the block map.

## -parameters

### -param blocks [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>**</b>

The enumerator for traversing the blocks.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>