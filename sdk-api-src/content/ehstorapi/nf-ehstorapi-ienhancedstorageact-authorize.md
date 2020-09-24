---
UID: NF:ehstorapi.IEnhancedStorageACT.Authorize
title: IEnhancedStorageACT::Authorize (ehstorapi.h)
description: Associates the Addressable Command Target (ACT) with the Authorized state defined by ACT_AUTHORIZATION_STATE, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.
helpviewer_keywords: ["Authorize","Authorize method [Enhanced Storage]","Authorize method [Enhanced Storage]","IEnhancedStorageACT interface","IEnhancedStorageACT interface [Enhanced Storage]","Authorize method","IEnhancedStorageACT.Authorize","IEnhancedStorageACT::Authorize","ehstorapi/IEnhancedStorageACT::Authorize","enstor.ienhancedstorageact_authorize"]
old-location: enstor\ienhancedstorageact_authorize.htm
tech.root: enstor
ms.assetid: 77141891-9adc-4cd9-b682-8f5b8e842f4c
ms.date: 12/05/2018
ms.keywords: Authorize, Authorize method [Enhanced Storage], Authorize method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],Authorize method, IEnhancedStorageACT.Authorize, IEnhancedStorageACT::Authorize, ehstorapi/IEnhancedStorageACT::Authorize, enstor.ienhancedstorageact_authorize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnhancedStorageACT::Authorize
 - ehstorapi/IEnhancedStorageACT::Authorize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageACT.Authorize
---

# IEnhancedStorageACT::Authorize


## -description

Associates the Addressable Command Target (ACT) with the <b>Authorized</b> state    defined by <a href="/windows/desktop/api/ehstorapi/ns-ehstorapi-act_authorization_state">ACT_AUTHORIZATION_STATE</a>, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.

## -parameters

### -param hwndParent [in]

Not used.

### -param dwFlags [in]

Not used.

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
Authorization completed successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The authorization operation has failed.

</td>
</tr>
</table>

## -remarks

This interface method can be used when an application wants to change the ACT to the 'Authorized' state.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>