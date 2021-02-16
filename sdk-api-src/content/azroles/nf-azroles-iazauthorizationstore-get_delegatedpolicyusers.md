---
UID: NF:azroles.IAzAuthorizationStore.get_DelegatedPolicyUsers
title: IAzAuthorizationStore::get_DelegatedPolicyUsers (azroles.h)
description: Retrieves the security identifiers (SIDs) of principals that act as delegated policy users in text form.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DelegatedPolicyUsers property","DelegatedPolicyUsers property [Security]","DelegatedPolicyUsers property [Security]","AzAuthorizationStore object","DelegatedPolicyUsers property [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DelegatedPolicyUsers property","IAzAuthorizationStore.DelegatedPolicyUsers","IAzAuthorizationStore.get_DelegatedPolicyUsers","IAzAuthorizationStore::DelegatedPolicyUsers","IAzAuthorizationStore::get_DelegatedPolicyUsers","azroles/IAzAuthorizationStore::DelegatedPolicyUsers","azroles/IAzAuthorizationStore::get_DelegatedPolicyUsers","get_DelegatedPolicyUsers","security.azauthorizationstore_delegatedpolicyusers"]
old-location: security\azauthorizationstore_delegatedpolicyusers.htm
tech.root: security
ms.assetid: cc1268d5-d386-4888-a987-e40896a096e4
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],DelegatedPolicyUsers property, DelegatedPolicyUsers property [Security], DelegatedPolicyUsers property [Security],AzAuthorizationStore object, DelegatedPolicyUsers property [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DelegatedPolicyUsers property, IAzAuthorizationStore.DelegatedPolicyUsers, IAzAuthorizationStore.get_DelegatedPolicyUsers, IAzAuthorizationStore::DelegatedPolicyUsers, IAzAuthorizationStore::get_DelegatedPolicyUsers, azroles/IAzAuthorizationStore::DelegatedPolicyUsers, azroles/IAzAuthorizationStore::get_DelegatedPolicyUsers, get_DelegatedPolicyUsers, security.azauthorizationstore_delegatedpolicyusers
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
 - IAzAuthorizationStore::get_DelegatedPolicyUsers
 - azroles/IAzAuthorizationStore::get_DelegatedPolicyUsers
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
 - IAzAuthorizationStore.DelegatedPolicyUsers
 - IAzAuthorizationStore.get_DelegatedPolicyUsers
 - AzAuthorizationStore.DelegatedPolicyUsers
---

# IAzAuthorizationStore::get_DelegatedPolicyUsers


## -description

The <b>DelegatedPolicyUsers</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) of principals that act as delegated policy users in text form.

This property is read-only.

## -parameters

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a>  or <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.