---
UID: NN:fhcfg.IFhScopeIterator
title: IFhScopeIterator (fhcfg.h)
author: windows-sdk-content
description: The IFhScopeIterator interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call the IFhConfigMgr::GetIncludeExcludeRules method.
old-location: winprog\ifhscopeiterator.htm
tech.root: DevNotes
ms.assetid: E8F993BD-CB53-474A-926D-AED0F5A17073
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFhScopeIterator, IFhScopeIterator interface [Windows API], IFhScopeIterator interface [Windows API],described, fhcfg/IFhScopeIterator, winprog.ifhscopeiterator
ms.topic: interface
f1_keywords: 
 - "fhcfg/IFhScopeIterator"
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - IFhScopeIterator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhScopeIterator interface


## -description


The <b>IFhScopeIterator</b> interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call  the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">IFhConfigMgr::GetIncludeExcludeRules</a> method.

> [!NOTE] 
> **IFhScopeIterator** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhScopeIterator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhScopeIterator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFhScopeIterator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhscopeiterator-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves the current item in an inclusion or exclusion list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhscopeiterator-movetonextitem">MoveToNextItem</a>
</td>
<td align="left" width="63%">
Moves to the next item in the inclusion or exclusion list.

</td>
</tr>
</table> 

