---
UID: NN:appxpackaging.IAppxBlockMapReader
title: IAppxBlockMapReader (appxpackaging.h)
description: Represents a read-only object model for block maps that provides access to the file attributes and block hashes.
helpviewer_keywords: ["IAppxBlockMapReader","IAppxBlockMapReader interface [App packaging and management]","IAppxBlockMapReader interface [App packaging and management]","described","appxpackaging/IAppxBlockMapReader","appxpkg.iappxblockmapreader"]
old-location: appxpkg\iappxblockmapreader.htm
tech.root: appxpkg
ms.assetid: 233539FD-E3BE-4783-9F23-B34F6397FBBE
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapReader, IAppxBlockMapReader interface [App packaging and management], IAppxBlockMapReader interface [App packaging and management],described, appxpackaging/IAppxBlockMapReader, appxpkg.iappxblockmapreader
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
 - IAppxBlockMapReader
 - appxpackaging/IAppxBlockMapReader
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
 - IAppxBlockMapReader
---

# IAppxBlockMapReader interface


## -description

Represents a read-only object model for block maps that provides access to the file attributes and block hashes.

## -inheritance

The <b>IAppxBlockMapReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapReader</b> also has these types of members:

## -remarks

The <b>IAppxBlockMapReader</b> represents the <b>BlockMap</b> root element of the block map. <b>File</b> elements are the child elements of the <b>BlockMap</b> element.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createblockmapreader">CreateBlockMapReader</a> or <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createvalidatedblockmapreader">CreateValidatedBlockMapReader</a> method of the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface, or the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getblockmap">GetBlockMap </a> method of the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a> interface.

For a code example, see the [Query app package and app manifest sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx).

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx">Query app package and app manifest sample</a>
