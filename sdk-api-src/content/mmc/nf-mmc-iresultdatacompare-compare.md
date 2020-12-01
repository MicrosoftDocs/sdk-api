---
UID: NF:mmc.IResultDataCompare.Compare
title: IResultDataCompare::Compare (mmc.h)
description: Provides a way for a primary snap-in to compare cookies for the purpose of sorting the result items that it inserts in the result pane.
helpviewer_keywords: ["Compare","Compare method [MMC]","Compare method [MMC]","IResultDataCompare interface","IResultDataCompare interface [MMC]","Compare method","IResultDataCompare.Compare","IResultDataCompare::Compare","_slate_iresultdatacompare_compare","mmc.iresultdatacompare_compare","mmc/IResultDataCompare::Compare"]
old-location: mmc\iresultdatacompare_compare.htm
tech.root: mmc
ms.assetid: 00d18ba5-589f-4a70-b331-ba9c7d5164c5
ms.date: 12/05/2018
ms.keywords: Compare, Compare method [MMC], Compare method [MMC],IResultDataCompare interface, IResultDataCompare interface [MMC],Compare method, IResultDataCompare.Compare, IResultDataCompare::Compare, _slate_iresultdatacompare_compare, mmc.iresultdatacompare_compare, mmc/IResultDataCompare::Compare
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResultDataCompare::Compare
 - mmc/IResultDataCompare::Compare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultDataCompare.Compare
---

# IResultDataCompare::Compare


## -description

The <b>IResultDataCompare::Compare</b> method provides a way for a primary snap-in to compare cookies for the purpose of sorting the result items that it inserts in the result pane.

The <b>IResultDataCompare::Compare</b> method cannot be used for scope items. However, this functionality is provided by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a> method.

## -parameters

### -param lUserParam [in]

A value that specifies user-provided information that is passed into 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-sort">IResultData::Sort</a>. MMC does not interpret this parameter.

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
<a href="/windows/desktop/api/mmc/nn-mmc-iresultownerdata">IResultOwnerData</a> interface to provide sorting for virtual lists.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-sort">IResultData::Sort</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultownerdata-sortitems">IResultOwnerData::SortItems</a>