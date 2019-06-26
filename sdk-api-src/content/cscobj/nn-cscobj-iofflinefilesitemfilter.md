---
UID: NN:cscobj.IOfflineFilesItemFilter
title: IOfflineFilesItemFilter (cscobj.h)
author: windows-sdk-content
description: Represents an instance of a filter to be applied to an enumeration.
old-location: of\iofflinefilesitemfilter.htm
tech.root: offlinefiles
ms.assetid: e77b4f90-7a08-47f8-b297-8c1360167e1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItemFilter, IOfflineFilesItemFilter interface [Offline Files], IOfflineFilesItemFilter interface [Offline Files],described, cscobj/IOfflineFilesItemFilter, of.iofflinefilesitemfilter
ms.topic: interface
f1_keywords: 
 - "cscobj/IOfflineFilesItemFilter"
req.header: cscobj.h
req.include-header: 
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesItemFilter interface


## -description


Represents an instance of a filter to be applied to an enumeration. For a complete description of filtering behavior, see the section titled "Item Filtering."


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItemFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesItemFilter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-getfilterflags">GetFilterFlags</a>
</td>
<td align="left" width="63%">
Provides flags to control flag-based filtering of items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-getpatternfilter">GetPatternFilter</a>
</td>
<td align="left" width="63%">
Provides a filter pattern string to limit enumerated items based on item name patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-gettimefilter">GetTimeFilter</a>
</td>
<td align="left" width="63%">
Provides time-value-comparison semantics to control filtering of items based on time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

