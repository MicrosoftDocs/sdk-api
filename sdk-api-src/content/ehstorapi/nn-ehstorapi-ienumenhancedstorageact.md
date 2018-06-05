---
UID: NN:ehstorapi.IEnumEnhancedStorageACT
title: IEnumEnhancedStorageACT
author: windows-sdk-content
description: Use this interface as the top level enumerator for all IEEE 1667 Addressable Contact Targets (ACT).
old-location: enstor\ienumenhancedstorageact.htm
old-project: enstor
ms.assetid: 807834cc-0f52-43f6-a3b3-06591ba68c15
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IEnumEnhancedStorageACT, IEnumEnhancedStorageACT interface [Enhanced Storage], IEnumEnhancedStorageACT interface [Enhanced Storage],described, ehstorapi/IEnumEnhancedStorageACT, enstor.ienumenhancedstorageact
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EhStorAPI.h
api_name:
-	IEnumEnhancedStorageACT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnumEnhancedStorageACT interface


## -description


Use this interface as the top level enumerator for all IEEE 1667 Addressable Contact Targets (ACT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumEnhancedStorageACT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumEnhancedStorageACT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/139bb8ed-faca-4fe7-ab6f-63c71d25a711">GetACTs</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the ACTs currently connected to the system. If at least one IEEE 1667 ACT is present, the Enhanced Storage API allocates an array of 1 or more <a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a> pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13c0475e-a73a-4e26-b6ec-6b9cb19e23f3">GetMatchingACT</a>
</td>
<td align="left" width="63%">
Returns the ACT associated with the volume specified via a string supplied by the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a>
 

 

