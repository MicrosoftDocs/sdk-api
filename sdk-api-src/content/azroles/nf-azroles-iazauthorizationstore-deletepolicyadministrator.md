---
UID: NF:azroles.IAzAuthorizationStore.DeletePolicyAdministrator
title: IAzAuthorizationStore::DeletePolicyAdministrator (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of principals that act as policy administrators.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DeletePolicyAdministrator method","DeletePolicyAdministrator","DeletePolicyAdministrator method [Security]","DeletePolicyAdministrator method [Security]","AzAuthorizationStore object","DeletePolicyAdministrator method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DeletePolicyAdministrator method","IAzAuthorizationStore.DeletePolicyAdministrator","IAzAuthorizationStore::DeletePolicyAdministrator","azroles/IAzAuthorizationStore::DeletePolicyAdministrator","security.azauthorizationstore_deletepolicyadministrator"]
old-location: security\azauthorizationstore_deletepolicyadministrator.htm
tech.root: security
ms.assetid: c27ca754-7808-4c96-8966-0be3960f2926
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],DeletePolicyAdministrator method, DeletePolicyAdministrator, DeletePolicyAdministrator method [Security], DeletePolicyAdministrator method [Security],AzAuthorizationStore object, DeletePolicyAdministrator method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeletePolicyAdministrator method, IAzAuthorizationStore.DeletePolicyAdministrator, IAzAuthorizationStore::DeletePolicyAdministrator, azroles/IAzAuthorizationStore::DeletePolicyAdministrator, security.azauthorizationstore_deletepolicyadministrator
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::DeletePolicyAdministrator
 - azroles/IAzAuthorizationStore::DeletePolicyAdministrator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - AzAuthorizationStore.DeletePolicyAdministrator
 - IAzAuthorizationStore.DeletePolicyAdministrator
---

# IAzAuthorizationStore::DeletePolicyAdministrator


## -description

The <b>DeletePolicyAdministrator</b> method removes the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Text form of the SID to remove from the list of policy administrators.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
To view the list of policy administrators, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyadministrators">PolicyAdministrators</a> property.