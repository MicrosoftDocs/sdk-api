---
UID: NN:appxpackaging.IAppxBlockMapBlock
title: IAppxBlockMapBlock
author: windows-sdk-content
description: The IAppxBlockMapBlock interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package.
old-location: appxpkg\iappxblockmapblock.htm
tech.root: appxpkg
ms.assetid: 39B0680A-F27B-478F-8E83-FE1BFCF61AC4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAppxBlockMapBlock, IAppxBlockMapBlock interface [App packaging and management], IAppxBlockMapBlock interface [App packaging and management],described, appxpackaging/IAppxBlockMapBlock, appxpkg.iappxblockmapblock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IAppxBlockMapBlock interface


## -description


The <b>IAppxBlockMapBlock</b> interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package. The <a href="https://msdn.microsoft.com/CE8FB813-B125-4FD6-A7C3-CA3ECA72ECE7">IAppxBlockMapFile::GetBlocks</a> method is used to return an enumerator for traversing and retrieving the individual blocks of a file listed in the package block map.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapBlock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBlockMapBlock</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/02B5F96E-EA8B-407F-98D8-BF6BFF72B346">GetCompressedSize</a>
</td>
<td align="left" width="63%">
Retrieves compressed size of the block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A8460C2-2BEE-4CEC-BAF4-779E6F58664D">GetHash</a>
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




<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>



<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>



<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>



<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

