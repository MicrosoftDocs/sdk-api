---
UID: NN:cscobj.IOfflineFilesItemFilter
title: IOfflineFilesItemFilter
author: windows-sdk-content
description: Represents an instance of a filter to be applied to an enumeration.
old-location: of\iofflinefilesitemfilter.htm
tech.root: OfflineFiles
ms.assetid: e77b4f90-7a08-47f8-b297-8c1360167e1f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesItemFilter, IOfflineFilesItemFilter interface [Offline Files], IOfflineFilesItemFilter interface [Offline Files],described, cscobj/IOfflineFilesItemFilter, of.iofflinefilesitemfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IOfflineFilesItemFilter interface


## -description


Represents an instance of a filter to be applied to an enumeration. For a complete description of filtering behavior, see the section titled "Item Filtering."


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItemFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesItemFilter</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530577(v=VS.85).aspx">GetFilterFlags</a>
</td>
<td align="left" width="63%">
Provides flags to control flag-based filtering of items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530578(v=VS.85).aspx">GetPatternFilter</a>
</td>
<td align="left" width="63%">
Provides a filter pattern string to limit enumerated items based on item name patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530579(v=VS.85).aspx">GetTimeFilter</a>
</td>
<td align="left" width="63%">
Provides time-value-comparison semantics to control filtering of items based on time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

