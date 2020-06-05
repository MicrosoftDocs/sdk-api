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
f1_keywords:
- appxpackaging/IAppxBlockMapReader
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
- IAppxBlockMapReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapReader interface


## -description


Represents a read-only object model for block maps that provides access to the file attributes and block hashes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapreader-getfile">GetFile</a>
</td>
<td align="left" width="63%">
Retrieves data corresponding to a file in the block map with the specified file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapreader-getfiles">GetFiles</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for traversing the files listed in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapreader-gethashmethod">GetHashMethod</a>
</td>
<td align="left" width="63%">
Retrieves the URI for the hash algorithm used to create block hashes in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapreader-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a read-only stream that represents the XML content of the block map.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBlockMapReader</b> represents the <b>BlockMap</b> root element of the block map. <b>File</b> elements are the child elements of the <b>BlockMap</b> element.

This object can be retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createblockmapreader">CreateBlockMapReader</a> or <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createvalidatedblockmapreader">CreateValidatedBlockMapReader</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface, or the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getblockmap">GetBlockMap </a>method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a> interface.

For a code example, see the [Query app package and app manifest sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx).

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx">Query app package and app manifest sample</a>


