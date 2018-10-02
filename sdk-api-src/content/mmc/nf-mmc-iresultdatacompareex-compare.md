---
UID: NF:mmc.IResultDataCompareEx.Compare
title: IResultDataCompareEx::Compare
author: windows-sdk-content
description: Provides a way for a primary snap-in to compare items for the purpose of sorting the scope and result items that it inserts in the result pane.
old-location: mmc\iresultdatacompareex_compare.htm
tech.root: MMC
ms.assetid: 0e3a8094-0d09-4a9c-8211-a0eb6a89ad55
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Compare, Compare method [MMC], Compare method [MMC],IResultDataCompareEx interface, IResultDataCompareEx interface [MMC],Compare method, IResultDataCompareEx.Compare, IResultDataCompareEx::Compare, _slate_iresultdatacompareex_compare, mmc.iresultdatacompareex_compare, mmc/IResultDataCompareEx::Compare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultDataCompareEx.Compare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultDataCompareEx::Compare


## -description


The <b>IResultDataCompareEx::Compare</b> method provides a way for a primary snap-in to compare items for the purpose of sorting the scope and result items that it inserts in the result pane.


## -parameters




### -param prdc [in]

A pointer to an 
<a href="https://msdn.microsoft.com/78f0648b-1d1b-4786-89fa-ef51b7743a2d">RDCOMPARE</a> structure that holds information about the items being compared and which column in the result pane list view is being sorted.


### -param pnResult [out]

The snap-in should set pnResult to the result of the comparison:

<ul>
<li>Any negative integer if item 1 &lt; item 2</li>
<li>Zero (0) if item 1 == item 2</li>
<li>Any positive integer if item 1 &gt; item 2</li>
</ul>

## -returns



This method can return one of these values.




## -remarks



Compare provides a mechanism for determining the sort order of scope and result item objects appearing in the result pane. The built-in sort provided by MMC only uses the C run-time library's string-compare function to compare the data. If this interface is implemented, it is used for all comparisons.

The comparison should be based on an ascending sort order. If the user toggles the standard result view header, the console complements the compare results, which results in a descending sort order.

The 
IResultDataCompareEx interface is not called for virtual list sorting. This is because the snap-in maintains all the item data storage for a virtual list, the snap-in must sort the items itself. A snap-in must implement the 
<a href="https://msdn.microsoft.com/184f3783-9000-45aa-867b-580800b560b3">IResultOwnerData</a> interface to provide sorting for virtual lists.



