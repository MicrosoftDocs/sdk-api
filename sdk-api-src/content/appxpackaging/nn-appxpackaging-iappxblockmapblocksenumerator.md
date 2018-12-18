---
UID: NN:appxpackaging.IAppxBlockMapBlocksEnumerator
title: IAppxBlockMapBlocksEnumerator
author: windows-sdk-content
description: Enumerates the blocks from a block map in a single file.
old-location: appxpkg\iappxblockmapblocksenumerator.htm
tech.root: appxpkg
ms.assetid: E7678755-4779-4A64-A666-C5FFC4A7F37A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxBlockMapBlocksEnumerator, IAppxBlockMapBlocksEnumerator interface [App packaging and management], IAppxBlockMapBlocksEnumerator interface [App packaging and management],described, appxpackaging/IAppxBlockMapBlocksEnumerator, appxpkg.iappxblockmapblocksenumerator
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
 - IAppxBlockMapBlocksEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBlockMapBlocksEnumerator interface


## -description


Enumerates the blocks  from a block map in a single file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapBlocksEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBlockMapBlocksEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapBlocksEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A546BD4D-DA7A-4A50-BD45-2219D70DF0F9">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the block at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC12BCDD-201C-4F22-B39E-1349EB84ED00">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a block at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CDF8C336-CFF8-41FE-AC3E-48988209850E">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next block.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>



<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>



<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>



<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

