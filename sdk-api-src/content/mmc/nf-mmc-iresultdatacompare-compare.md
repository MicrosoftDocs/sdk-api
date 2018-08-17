---
UID: NF:mmc.IResultDataCompare.Compare
title: IResultDataCompare::Compare
author: windows-sdk-content
description: Provides a way for a primary snap-in to compare cookies for the purpose of sorting the result items that it inserts in the result pane.
old-location: mmc\iresultdatacompare_compare.htm
old-project: mmc
ms.assetid: 00d18ba5-589f-4a70-b331-ba9c7d5164c5
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: Compare, Compare method [MMC], Compare method [MMC],IResultDataCompare interface, IResultDataCompare interface [MMC],Compare method, IResultDataCompare.Compare, IResultDataCompare::Compare, _slate_iresultdatacompare_compare, mmc.iresultdatacompare_compare, mmc/IResultDataCompare::Compare
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
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
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultDataCompare.Compare
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IResultDataCompare::Compare


## -description


The <b>IResultDataCompare::Compare</b> method provides a way for a primary snap-in to compare cookies for the purpose of sorting the result items that it inserts in the result pane.

The <b>IResultDataCompare::Compare</b> method cannot be used for scope items. However, this functionality is provided by the 
<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a> method.


## -parameters




### -param lUserParam [in]

A value that specifies user-provided information that is passed into 
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>. MMC does not interpret this parameter.


### -param cookieA [in]

The unique identifier of the first result item object to be compared as part of the sorting operation.


### -param cookieB [in]

The unique identifier of the second result item object to be compared as part of the sorting operation.


### -param pnResult [in, out]

As an in parameter, the argument contains the column that is sorted. As an out parameter, the value of the argument should be:

<ul>
<li>-1 if item 1 &lt; item 2</li>
<li>zero (0) if item 1 == item 2</li>
<li>1 if item 1 &gt; item 2</li>
</ul>

## -returns



This method can return one of these values.




## -remarks



Compare provides a mechanism for determining the sort order of result item objects appearing in the result pane. The built-in sort provided by MMC only uses the C run-time library string-compare function to compare the data. If this interface is implemented, it is used for all comparisons.

The comparison should be based on an ascending sort order. If the user toggles the standard result view header, the console complements the compare results, which results in a descending sort order.

This 
IResultDataCompare interface is not called for virtual list sorting. Because the snap-in maintains all the item data storage for a virtual list, the snap-in must sort the items itself. A snap-in must implement the 
<a href="https://msdn.microsoft.com/184f3783-9000-45aa-867b-580800b560b3">IResultOwnerData</a> interface to provide sorting for virtual lists.




## -see-also




<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>



<a href="https://msdn.microsoft.com/5326e935-cb6c-4f76-8c9b-87d910dbbb0d">IResultOwnerData::SortItems</a>
 

 

