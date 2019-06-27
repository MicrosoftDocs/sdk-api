---
UID: NN:appxpackaging.IAppxBlockMapBlock
title: IAppxBlockMapBlock (appxpackaging.h)
author: windows-sdk-content
description: The IAppxBlockMapBlock interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package.
old-location: appxpkg\iappxblockmapblock.htm
tech.root: appxpkg
ms.assetid: 39B0680A-F27B-478F-8E83-FE1BFCF61AC4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapBlock, IAppxBlockMapBlock interface [App packaging and management], IAppxBlockMapBlock interface [App packaging and management],described, appxpackaging/IAppxBlockMapBlock, appxpkg.iappxblockmapblock
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxBlockMapBlock"
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
 - IAppxBlockMapBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapBlock interface


## -description


The <b>IAppxBlockMapBlock</b> interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package. The <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getblocks">IAppxBlockMapFile::GetBlocks</a> method is used to return an enumerator for traversing and retrieving the individual blocks of a file listed in the package block map.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapBlock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapBlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapBlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapblock-getcompressedsize">GetCompressedSize</a>
</td>
<td align="left" width="63%">
Retrieves compressed size of the block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapblock-gethash">GetHash</a>
</td>
<td align="left" width="63%">
Retrieves the hash value of the block.

</td>
</tr>
</table> 


## -remarks



Each <b>Block</b> element has an attribute for the hash value and compressed size of the block.


#### Examples

For a example code, see <a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

