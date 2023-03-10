---
UID: NN:appxpackaging.IAppxBlockMapBlock
title: IAppxBlockMapBlock (appxpackaging.h)
description: The IAppxBlockMapBlock interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package.
helpviewer_keywords: ["IAppxBlockMapBlock","IAppxBlockMapBlock interface [App packaging and management]","IAppxBlockMapBlock interface [App packaging and management]","described","appxpackaging/IAppxBlockMapBlock","appxpkg.iappxblockmapblock"]
old-location: appxpkg\iappxblockmapblock.htm
tech.root: appxpkg
ms.assetid: 39B0680A-F27B-478F-8E83-FE1BFCF61AC4
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapBlock, IAppxBlockMapBlock interface [App packaging and management], IAppxBlockMapBlock interface [App packaging and management],described, appxpackaging/IAppxBlockMapBlock, appxpkg.iappxblockmapblock
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
 - IAppxBlockMapBlock
 - appxpackaging/IAppxBlockMapBlock
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
 - IAppxBlockMapBlock
---

# IAppxBlockMapBlock interface


## -description

The <b>IAppxBlockMapBlock</b> interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package. The <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getblocks">IAppxBlockMapFile::GetBlocks</a> method is used to return an enumerator for traversing and retrieving the individual blocks of a file listed in the package block map.

## -inheritance

The <b>IAppxBlockMapBlock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapBlock</b> also has these types of members:

## -remarks

Each <b>Block</b> element has an attribute for the hash value and compressed size of the block.

For a code example, see the [Query app package and app manifest sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx).

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx">Query app package and app manifest sample</a>
