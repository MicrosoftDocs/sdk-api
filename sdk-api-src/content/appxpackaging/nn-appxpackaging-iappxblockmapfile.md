---
UID: NN:appxpackaging.IAppxBlockMapFile
title: IAppxBlockMapFile (appxpackaging.h)
description: Represents a file in the block map.
old-location: appxpkg\iappxblockmapfile.htm
tech.root: appxpkg
ms.assetid: 4C380E2F-8125-4147-97F5-BEDF5BEFB81D
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapFile, IAppxBlockMapFile interface [App packaging and management], IAppxBlockMapFile interface [App packaging and management],described, appxpackaging/IAppxBlockMapFile, appxpkg.iappxblockmapfile
f1_keywords:
- appxpackaging/IAppxBlockMapFile
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
- IAppxBlockMapFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFile interface


## -description


Represents a file in the block map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapFile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getblocks">GetBlocks</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for traversing the blocks of a file listed in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getlocalfileheadersize">GetLocalFileHeaderSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the zip local file header of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-getuncompressedsize">GetUncompressedSize</a>
</td>
<td align="left" width="63%">
Retrieves the uncompressed size of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfile-validatefilehash">ValidateFileHash</a>
</td>
<td align="left" width="63%">
Validates the content of a file against the hashes stored in the block elements for this block map file.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBlockMapFile</b> interface provides a read-only object model that represents the files in the block map. Files are represented in the block map file with the <b>File</b> element. You can retrieve the file's attributes and block hashes from the <b>File</b> element. Block hashes can be obtained from the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a> interface.


#### Examples

For a example code, see <a href="https://code.msdn.microsoft.com/windowsdesktop/Appx-Packaging-API-3ff13a92">Read app package manifest info sample (DescribeAppx)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="https://code.msdn.microsoft.com/windowsdesktop/Appx-Packaging-API-3ff13a92">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

