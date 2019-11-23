---
UID: NN:appxpackaging.IAppxBlockMapBlocksEnumerator
title: IAppxBlockMapBlocksEnumerator (appxpackaging.h)

description: Enumerates the blocks from a block map in a single file.
old-location: appxpkg\iappxblockmapblocksenumerator.htm
tech.root: appxpkg
ms.assetid: E7678755-4779-4A64-A666-C5FFC4A7F37A

ms.date: 12/05/2018
ms.keywords: IAppxBlockMapBlocksEnumerator, IAppxBlockMapBlocksEnumerator interface [App packaging and management], IAppxBlockMapBlocksEnumerator interface [App packaging and management],described, appxpackaging/IAppxBlockMapBlocksEnumerator, appxpkg.iappxblockmapblocksenumerator
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxBlockMapBlocksEnumerator"
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
 - IAppxBlockMapBlocksEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapBlocksEnumerator interface


## -description


Enumerates the blocks  from a block map in a single file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapBlocksEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapBlocksEnumerator</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapblocksenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the block at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapblocksenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a block at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapblocksenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next block.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

