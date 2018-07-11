---
UID: NN:fhcfg.IFhScopeIterator
title: IFhScopeIterator
author: windows-sdk-content
description: The IFhScopeIterator interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call the IFhConfigMgr::GetIncludeExcludeRules method.
old-location: winprog\ifhscopeiterator.htm
old-project: DevNotes
ms.assetid: E8F993BD-CB53-474A-926D-AED0F5A17073
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IFhScopeIterator, IFhScopeIterator interface [Windows API], IFhScopeIterator interface [Windows API],described, fhcfg/IFhScopeIterator, winprog.ifhscopeiterator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhScopeIterator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhScopeIterator interface


## -description


The <b>IFhScopeIterator</b> interface allows client applications to enumerate individual items in an inclusion or exclusion list. To retrieve inclusion and exclusion lists, call  the <a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhScopeIterator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFhScopeIterator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/EB732725-497C-4D58-A05C-373732054BE5">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves the current item in an inclusion or exclusion list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A">MoveToNextItem</a>
</td>
<td align="left" width="63%">
Moves to the next item in the inclusion or exclusion list.

</td>
</tr>
</table> 

