---
UID: NN:mmc.IResultDataCompareEx
title: IResultDataCompareEx (mmc.h)
description: Allows primary snap-ins to compare both scope and result items that are displayed in a sorted order in the result pane.
helpviewer_keywords: ["IResultDataCompareEx","IResultDataCompareEx interface [MMC]","IResultDataCompareEx interface [MMC]","described","_slate_iresultdatacompareex","mmc.iresultdatacompareex","mmc/IResultDataCompareEx"]
old-location: mmc\iresultdatacompareex.htm
tech.root: mmc
ms.assetid: e4b305e4-4649-42f4-86f4-3c12e5aa5337
ms.date: 12/05/2018
ms.keywords: IResultDataCompareEx, IResultDataCompareEx interface [MMC], IResultDataCompareEx interface [MMC],described, _slate_iresultdatacompareex, mmc.iresultdatacompareex, mmc/IResultDataCompareEx
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
 - IResultDataCompareEx
 - mmc/IResultDataCompareEx
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
 - IResultDataCompareEx
---

# IResultDataCompareEx interface


## -description

The 
<b>IResultDataCompareEx</b> interface is introduced in MMC 1.2.

The 
<b>IResultDataCompareEx</b> interface allows primary snap-ins to compare both scope and result items that are displayed in a sorted order in the result pane. MMC uses a primary snap-in's implementation of this interface for all scope and result items. Any scope items inserted by extension snap-ins are left unsorted at the bottom of the list.

The 
<b>IResultDataCompareEx</b> interface differs from the 
<b>IResultDataCompareEx</b> interface. 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iresultdatacompare">IResultDataCompare</a> allows primary snap-ins to compare only result items. Scope items from either the primary snap-in or any extensions are left unsorted at the top of the list.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultDataCompareEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultDataCompareEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultDataCompareEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">Compare</a>
</td>
<td align="left" width="63%">
Compares two result view items.

</td>
</tr>
</table>

