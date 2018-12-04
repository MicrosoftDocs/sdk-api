---
UID: NN:appxpackaging.IAppxBlockMapFilesEnumerator
title: IAppxBlockMapFilesEnumerator
author: windows-sdk-content
description: Enumerates the files from a block map.
old-location: appxpkg\iappxblockmapfilesenumerator.htm
tech.root: appxpkg
ms.assetid: AC2E55C3-1EEF-4867-BECC-37F6269029D6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAppxBlockMapFilesEnumerator, IAppxBlockMapFilesEnumerator interface [App packaging and management], IAppxBlockMapFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxBlockMapFilesEnumerator, appxpkg.iappxblockmapfilesenumerator
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
 - IAppxBlockMapFilesEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBlockMapFilesEnumerator interface


## -description


Enumerates the files from a block map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapFilesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBlockMapFilesEnumerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6911EBF6-6D0A-4BA5-AD88-3F173141FA5B">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B0021CBC-9A3F-4D2D-8898-FE797396B312">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C50F7801-4C33-46EA-989C-259BA407C96B">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>



<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>



<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>



<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 

