---
UID: NN:ehstorapi.IEnhancedStorageACT
title: IEnhancedStorageACT (ehstorapi.h)
description: This interface to obtain information and perform operations for an 1667 Addressable Contact Target (ACT).
old-location: enstor\ienhancedstorageact.htm
tech.root: enstor
ms.assetid: 33d5df30-f877-4852-ad2f-af1bb58d0044
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageACT, IEnhancedStorageACT interface [Enhanced Storage], IEnhancedStorageACT interface [Enhanced Storage],described, ehstorapi/IEnhancedStorageACT, enstor.ienhancedstorageact
f1_keywords:
- ehstorapi/IEnhancedStorageACT
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
- IEnhancedStorageACT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnhancedStorageACT interface


## -description


Use this interface to obtain information and perform operations for an 1667 Addressable Contact Target (ACT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageACT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnhancedStorageACT</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstorageact-authorize">Authorize</a>
</td>
<td align="left" width="63%">
Associates the Addressable Command Target (ACT) with the <b>Authorized</b> state    defined by <a href="https://docs.microsoft.com/windows/desktop/api/ehstorapi/ns-ehstorapi-act_authorization_state">ACT_AUTHORIZATION_STATE</a>, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstorageact-getauthorizationstate">GetAuthorizationState</a>
</td>
<td align="left" width="63%">
Returns the current authorization state of the ACT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstorageact-getsilos">GetSilos</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all the silos associated with the ACT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstorageact-getuniqueidentity">GetUniqueIdentity</a>
</td>
<td align="left" width="63%">
Retrieves the unique identity of the Addressable Command Target (ACT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstorageact-unauthorize">Unauthorize</a>
</td>
<td align="left" width="63%">
Associates the Addressable Command Target (ACT) with the <b>Unauthorized</b> state defined by <a href="https://docs.microsoft.com/windows/desktop/api/ehstorapi/ns-ehstorapi-act_authorization_state">ACT_AUTHORIZATION_STATE</a>, and ensures the deauthentication of each individual silo according to the required sequence and logical combination necessary to unauthorize access to the ACT.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienumenhancedstorageact">IEnumEnhancedStorageACT</a>
 

 

