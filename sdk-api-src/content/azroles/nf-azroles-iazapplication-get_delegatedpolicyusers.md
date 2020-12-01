---
UID: NF:azroles.IAzApplication.get_DelegatedPolicyUsers
title: IAzApplication::get_DelegatedPolicyUsers (azroles.h)
description: Retrieves the security identifiers (SIDs), in text form, of principals that act as delegated policy users.
helpviewer_keywords: ["AzApplication object [Security]","DelegatedPolicyUsers property","DelegatedPolicyUsers property [Security]","DelegatedPolicyUsers property [Security]","AzApplication object","DelegatedPolicyUsers property [Security]","IAzApplication interface","IAzApplication interface [Security]","DelegatedPolicyUsers property","IAzApplication.DelegatedPolicyUsers","IAzApplication.get_DelegatedPolicyUsers","IAzApplication::DelegatedPolicyUsers","IAzApplication::get_DelegatedPolicyUsers","azroles/IAzApplication::DelegatedPolicyUsers","azroles/IAzApplication::get_DelegatedPolicyUsers","get_DelegatedPolicyUsers","security.iazapplication_delegatedpolicyusers"]
old-location: security\iazapplication_delegatedpolicyusers.htm
tech.root: security
ms.assetid: b20e1d5c-b07e-4f75-8b63-38036b07b24d
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DelegatedPolicyUsers property, DelegatedPolicyUsers property [Security], DelegatedPolicyUsers property [Security],AzApplication object, DelegatedPolicyUsers property [Security],IAzApplication interface, IAzApplication interface [Security],DelegatedPolicyUsers property, IAzApplication.DelegatedPolicyUsers, IAzApplication.get_DelegatedPolicyUsers, IAzApplication::DelegatedPolicyUsers, IAzApplication::get_DelegatedPolicyUsers, azroles/IAzApplication::DelegatedPolicyUsers, azroles/IAzApplication::get_DelegatedPolicyUsers, get_DelegatedPolicyUsers, security.iazapplication_delegatedpolicyusers
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
 - IAzApplication::get_DelegatedPolicyUsers
 - azroles/IAzApplication::get_DelegatedPolicyUsers
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
 - IAzApplication.DelegatedPolicyUsers
 - IAzApplication.get_DelegatedPolicyUsers
 - AzApplication.DelegatedPolicyUsers
---

# IAzApplication::get_DelegatedPolicyUsers


## -description

The <b>DelegatedPolicyUsers</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of principals that act as delegated policy users.

This property is read-only.

## -parameters

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.