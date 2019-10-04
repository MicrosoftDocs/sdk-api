---
UID: NN:ehstorapi.IEnumEnhancedStorageACT
title: IEnumEnhancedStorageACT (ehstorapi.h)
author: windows-sdk-content
description: Use this interface as the top level enumerator for all IEEE 1667 Addressable Contact Targets (ACT).
old-location: enstor\ienumenhancedstorageact.htm
tech.root: enstor
ms.assetid: 807834cc-0f52-43f6-a3b3-06591ba68c15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumEnhancedStorageACT, IEnumEnhancedStorageACT interface [Enhanced Storage], IEnumEnhancedStorageACT interface [Enhanced Storage],described, ehstorapi/IEnumEnhancedStorageACT, enstor.ienumenhancedstorageact
ms.topic: interface
f1_keywords: 
 - "ehstorapi/IEnumEnhancedStorageACT"
dev_langs:
 - c++
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - EhStorAPI.h
api_name:
 - IEnumEnhancedStorageACT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumEnhancedStorageACT interface


## -description


Use this interface as the top level enumerator for all IEEE 1667 Addressable Contact Targets (ACT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumEnhancedStorageACT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumEnhancedStorageACT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumEnhancedStorageACT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienumenhancedstorageact-getacts">GetACTs</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the ACTs currently connected to the system. If at least one IEEE 1667 ACT is present, the Enhanced Storage API allocates an array of 1 or more <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a> pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienumenhancedstorageact-getmatchingact">GetMatchingACT</a>
</td>
<td align="left" width="63%">
Returns the ACT associated with the volume specified via a string supplied by the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>
 

 

