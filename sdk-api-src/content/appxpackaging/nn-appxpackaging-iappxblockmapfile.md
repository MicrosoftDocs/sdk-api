---
UID: NN:appxpackaging.IAppxBlockMapFile
title: IAppxBlockMapFile (appxpackaging.h)
description: Represents a file in the block map.
helpviewer_keywords: ["IAppxBlockMapFile","IAppxBlockMapFile interface [App packaging and management]","IAppxBlockMapFile interface [App packaging and management]","described","appxpackaging/IAppxBlockMapFile","appxpkg.iappxblockmapfile"]
old-location: appxpkg\iappxblockmapfile.htm
tech.root: appxpkg
ms.assetid: 4C380E2F-8125-4147-97F5-BEDF5BEFB81D
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapFile, IAppxBlockMapFile interface [App packaging and management], IAppxBlockMapFile interface [App packaging and management],described, appxpackaging/IAppxBlockMapFile, appxpkg.iappxblockmapfile
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
 - IAppxBlockMapFile
 - appxpackaging/IAppxBlockMapFile
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
 - IAppxBlockMapFile
---

# IAppxBlockMapFile interface


## -description

Represents a file in the block map.

## -inheritance

The <b>IAppxBlockMapFile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapFile</b> also has these types of members:

## -remarks

The <b>IAppxBlockMapFile</b> interface provides a read-only object model that represents the files in the block map. Files are represented in the block map file with the <b>File</b> element. You can retrieve the file's attributes and block hashes from the <b>File</b> element. Block hashes can be obtained from the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a> interface.

For a code example, see the [Query app package and app manifest sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx).

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx">Query app package and app manifest sample</a>
