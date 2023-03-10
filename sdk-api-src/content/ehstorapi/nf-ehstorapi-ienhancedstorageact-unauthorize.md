---
UID: NF:ehstorapi.IEnhancedStorageACT.Unauthorize
title: IEnhancedStorageACT::Unauthorize (ehstorapi.h)
description: Associates the Addressable Command Target (ACT) with the Unauthorized state defined by ACT_AUTHORIZATION_STATE, and ensures the deauthentication of each individual silo according to the required sequence and logical combination necessary to restrict access to the ACT.
helpviewer_keywords: ["IEnhancedStorageACT interface [Enhanced Storage]","Unauthorize method","IEnhancedStorageACT.Unauthorize","IEnhancedStorageACT::Unauthorize","Unauthorize","Unauthorize method [Enhanced Storage]","Unauthorize method [Enhanced Storage]","IEnhancedStorageACT interface","ehstorapi/IEnhancedStorageACT::Unauthorize","enstor.ienhancedstorageact_unauthorize"]
old-location: enstor\ienhancedstorageact_unauthorize.htm
tech.root: enstor
ms.assetid: 82f78f9d-fb50-4f44-b4ad-f3a43ccca671
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageACT interface [Enhanced Storage],Unauthorize method, IEnhancedStorageACT.Unauthorize, IEnhancedStorageACT::Unauthorize, Unauthorize, Unauthorize method [Enhanced Storage], Unauthorize method [Enhanced Storage],IEnhancedStorageACT interface, ehstorapi/IEnhancedStorageACT::Unauthorize, enstor.ienhancedstorageact_unauthorize
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
 - IEnhancedStorageACT::Unauthorize
 - ehstorapi/IEnhancedStorageACT::Unauthorize
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
 - IEnhancedStorageACT.Unauthorize
---

# IEnhancedStorageACT::Unauthorize


## -description

Associates the Addressable Command Target (ACT) with the <b>Unauthorized</b> state defined by <a href="/windows/desktop/api/ehstorapi/ns-ehstorapi-act_authorization_state">ACT_AUTHORIZATION_STATE</a>, and ensures the deauthentication of each individual silo according to the required sequence and logical combination necessary to restrict access to the ACT.



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
Unauthorization completed successfully.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>
