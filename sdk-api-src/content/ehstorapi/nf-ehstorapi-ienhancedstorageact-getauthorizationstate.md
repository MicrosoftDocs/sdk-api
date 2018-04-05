---
UID: NF:ehstorapi.IEnhancedStorageACT.GetAuthorizationState
title: IEnhancedStorageACT::GetAuthorizationState method
author: windows-driver-content
description: Returns the current authorization state of the ACT.
old-location: enstor\ienhancedstorageact_getauthorizationstate.htm
old-project: enstor
ms.assetid: 79615cae-cdd1-43bc-9954-108084ea692b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAuthorizationState method [Enhanced Storage], GetAuthorizationState method [Enhanced Storage], IEnhancedStorageACT interface, GetAuthorizationState,IEnhancedStorageACT.GetAuthorizationState, IEnhancedStorageACT, IEnhancedStorageACT interface [Enhanced Storage], GetAuthorizationState method, IEnhancedStorageACT::GetAuthorizationState, ehstorapi/IEnhancedStorageACT::GetAuthorizationState, enstor.ienhancedstorageact_getauthorizationstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EhStorAPI.h
api_name:
-	IEnhancedStorageACT.GetAuthorizationState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageACT::GetAuthorizationState method


## -description


Returns the current authorization state of the ACT.


## -parameters




### -param pState [out]

Pointer to a <a href="https://msdn.microsoft.com/385b2f9d-659e-451d-97da-15be70180e1f">ACT_AUTHORIZATION_STATE</a> that specifies the current authorization state of the ACT. 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
The current authorization state was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pState</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a>
 

 

