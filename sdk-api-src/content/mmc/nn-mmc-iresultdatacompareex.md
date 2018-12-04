---
UID: NN:mmc.IResultDataCompareEx
title: IResultDataCompareEx
author: windows-sdk-content
description: Allows primary snap-ins to compare both scope and result items that are displayed in a sorted order in the result pane.
old-location: mmc\iresultdatacompareex.htm
tech.root: mmc
ms.assetid: e4b305e4-4649-42f4-86f4-3c12e5aa5337
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IResultDataCompareEx, IResultDataCompareEx interface [MMC], IResultDataCompareEx interface [MMC],described, _slate_iresultdatacompareex, mmc.iresultdatacompareex, mmc/IResultDataCompareEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IResultDataCompareEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/7a68713c-2de5-4944-a617-0b2d46c23eea">IResultDataCompare</a> allows primary snap-ins to compare only result items. Scope items from either the primary snap-in or any extensions are left unsorted at the top of the list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultDataCompareEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultDataCompareEx</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">Compare</a>
</td>
<td align="left" width="63%">
Compares two result view items.

</td>
</tr>
</table> 

