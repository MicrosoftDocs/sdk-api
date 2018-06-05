---
UID: NN:ehstorapi.IEnhancedStorageACT
title: IEnhancedStorageACT
author: windows-sdk-content
description: This interface to obtain information and perform operations for an 1667 Addressable Contact Target (ACT).
old-location: enstor\ienhancedstorageact.htm
old-project: enstor
ms.assetid: 33d5df30-f877-4852-ad2f-af1bb58d0044
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IEnhancedStorageACT, IEnhancedStorageACT interface [Enhanced Storage], IEnhancedStorageACT interface [Enhanced Storage],described, ehstorapi/IEnhancedStorageACT, enstor.ienhancedstorageact
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
-	IEnhancedStorageACT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageACT interface


## -description


Use this interface to obtain information and perform operations for an 1667 Addressable Contact Target (ACT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageACT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnhancedStorageACT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnhancedStorageACT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77141891-9adc-4cd9-b682-8f5b8e842f4c">Authorize</a>
</td>
<td align="left" width="63%">
Associates the Addressable Command Target (ACT) with the <b>Authorized</b> state    defined by <a href="https://msdn.microsoft.com/385b2f9d-659e-451d-97da-15be70180e1f">ACT_AUTHORIZATION_STATE</a>, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79615cae-cdd1-43bc-9954-108084ea692b">GetAuthorizationState</a>
</td>
<td align="left" width="63%">
Returns the current authorization state of the ACT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/823da812-b3f5-4c61-bb33-cd970695879f">GetSilos</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the silos associated with the ACT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f8d33af-a771-4cbd-9740-a72fbb7e9b42">GetUniqueIdentity</a>
</td>
<td align="left" width="63%">
Retrieves the unique identity of the Addressable Command Target (ACT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f78f9d-fb50-4f44-b4ad-f3a43ccca671">Unauthorize</a>
</td>
<td align="left" width="63%">
Associates the Addressable Command Target (ACT) with the <b>Unauthorized</b> state defined by <a href="https://msdn.microsoft.com/385b2f9d-659e-451d-97da-15be70180e1f">ACT_AUTHORIZATION_STATE</a>, and ensures the deauthentication of each individual silo according to the required sequence and logical combination necessary to unauthorize access to the ACT.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/807834cc-0f52-43f6-a3b3-06591ba68c15">IEnumEnhancedStorageACT</a>
 

 

