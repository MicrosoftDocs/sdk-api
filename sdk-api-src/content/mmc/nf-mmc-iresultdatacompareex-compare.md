---
UID: NF:mmc.IResultDataCompareEx.Compare
title: IResultDataCompareEx::Compare (mmc.h)
description: Provides a way for a primary snap-in to compare items for the purpose of sorting the scope and result items that it inserts in the result pane.
helpviewer_keywords: ["Compare","Compare method [MMC]","Compare method [MMC]","IResultDataCompareEx interface","IResultDataCompareEx interface [MMC]","Compare method","IResultDataCompareEx.Compare","IResultDataCompareEx::Compare","_slate_iresultdatacompareex_compare","mmc.iresultdatacompareex_compare","mmc/IResultDataCompareEx::Compare"]
old-location: mmc\iresultdatacompareex_compare.htm
tech.root: mmc
ms.assetid: 0e3a8094-0d09-4a9c-8211-a0eb6a89ad55
ms.date: 12/05/2018
ms.keywords: Compare, Compare method [MMC], Compare method [MMC],IResultDataCompareEx interface, IResultDataCompareEx interface [MMC],Compare method, IResultDataCompareEx.Compare, IResultDataCompareEx::Compare, _slate_iresultdatacompareex_compare, mmc.iresultdatacompareex_compare, mmc/IResultDataCompareEx::Compare
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
 - IResultDataCompareEx::Compare
 - mmc/IResultDataCompareEx::Compare
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
 - IResultDataCompareEx.Compare
---

# IResultDataCompareEx::Compare


## -description

The <b>IResultDataCompareEx::Compare</b> method provides a way for a primary snap-in to compare items for the purpose of sorting the scope and result items that it inserts in the result pane.

## -parameters

### -param prdc [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-rdcompare">RDCOMPARE</a> structure that holds information about the items being compared and which column in the result pane list view is being sorted.

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
<a href="/windows/desktop/api/mmc/nn-mmc-iresultownerdata">IResultOwnerData</a> interface to provide sorting for virtual lists.