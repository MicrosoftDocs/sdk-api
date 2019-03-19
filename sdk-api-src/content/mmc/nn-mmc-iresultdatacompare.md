---
UID: NN:mmc.IResultDataCompare
title: IResultDataCompare (mmc.h)
author: windows-sdk-content
description: Allows primary snap-ins to compare result items that are displayed in a sorted order in the result pane.
old-location: mmc\iresultdatacompare.htm
tech.root: mmc
ms.assetid: 7a68713c-2de5-4944-a617-0b2d46c23eea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IResultDataCompare, IResultDataCompare interface [MMC], IResultDataCompare interface [MMC],described, _slate_iresultdatacompare, mmc.iresultdatacompare, mmc/IResultDataCompare
ms.topic: interface
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
 - IResultDataCompare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultDataCompare interface


## -description


The 
<b>IResultDataCompare</b> interface allows primary snap-ins to compare result items that are displayed in a sorted order in the result pane. MMC uses a primary snap-in's implementation of this interface for all results items. Scope items from either the primary snap-in or any extensions are left unsorted at the top of the list.

The 
<b>IResultDataCompare</b> interface differs from the 
<a href="https://msdn.microsoft.com/e4b305e4-4649-42f4-86f4-3c12e5aa5337">IResultDataCompareEx</a> interface. 
<b>IResultDataCompareEx</b> allows primary snap-ins to compare both scope and result items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultDataCompare</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultDataCompare</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultDataCompare</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00d18ba5-589f-4a70-b331-ba9c7d5164c5">Compare</a>
</td>
<td align="left" width="63%">
Compares two cookies.

</td>
</tr>
</table> 

