---
UID: NN:appxpackaging.IAppxBlockMapFilesEnumerator
title: IAppxBlockMapFilesEnumerator (appxpackaging.h)
author: windows-sdk-content
description: Enumerates the files from a block map.
old-location: appxpkg\iappxblockmapfilesenumerator.htm
tech.root: appxpkg
ms.assetid: AC2E55C3-1EEF-4867-BECC-37F6269029D6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapFilesEnumerator, IAppxBlockMapFilesEnumerator interface [App packaging and management], IAppxBlockMapFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxBlockMapFilesEnumerator, appxpkg.iappxblockmapfilesenumerator
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxBlockMapFilesEnumerator"
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
 - IAppxBlockMapFilesEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFilesEnumerator interface


## -description


Enumerates the files from a block map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapFilesEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBlockMapFilesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapFilesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfilesenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfilesenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxblockmapfilesenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblocksenumerator">IAppxBlockMapBlocksEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapreader">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

