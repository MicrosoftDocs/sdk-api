---
UID: NN:cscobj.IOfflineFilesItemFilter
title: IOfflineFilesItemFilter
author: windows-sdk-content
description: Represents an instance of a filter to be applied to an enumeration.
old-location: of\iofflinefilesitemfilter.htm
old-project: offlinefiles
ms.assetid: e77b4f90-7a08-47f8-b297-8c1360167e1f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesItemFilter, IOfflineFilesItemFilter interface [Offline Files], IOfflineFilesItemFilter interface [Offline Files],described, cscobj/IOfflineFilesItemFilter, of.iofflinefilesitemfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesItemFilter interface


## -description


Represents an instance of a filter to be applied to an enumeration. For a complete description of filtering behavior, see the section titled "Item Filtering."


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItemFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesItemFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesItemFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75466fc7-d14c-4ce7-82e9-9622287a50d1">GetFilterFlags</a>
</td>
<td align="left" width="63%">
Provides flags to control flag-based filtering of items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/570cf25c-d4a4-42d6-8f33-bb660a7e99ab">GetPatternFilter</a>
</td>
<td align="left" width="63%">
Provides a filter pattern string to limit enumerated items based on item name patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/397611e7-60e5-46d6-b90b-5aed7fff6a43">GetTimeFilter</a>
</td>
<td align="left" width="63%">
Provides time-value-comparison semantics to control filtering of items based on time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

