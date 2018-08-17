---
UID: NF:azroles.IAzAuthorizationStore.get_DelegatedPolicyUsers
title: IAzAuthorizationStore::get_DelegatedPolicyUsers
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs) of principals that act as delegated policy users in text form.
old-location: security\azauthorizationstore_delegatedpolicyusers.htm
old-project: secauthz
ms.assetid: cc1268d5-d386-4888-a987-e40896a096e4
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzAuthorizationStore object [Security],DelegatedPolicyUsers property, DelegatedPolicyUsers property [Security], DelegatedPolicyUsers property [Security],AzAuthorizationStore object, DelegatedPolicyUsers property [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DelegatedPolicyUsers property, IAzAuthorizationStore.DelegatedPolicyUsers, IAzAuthorizationStore.get_DelegatedPolicyUsers, IAzAuthorizationStore::DelegatedPolicyUsers, IAzAuthorizationStore::get_DelegatedPolicyUsers, azroles/IAzAuthorizationStore::DelegatedPolicyUsers, azroles/IAzAuthorizationStore::get_DelegatedPolicyUsers, get_DelegatedPolicyUsers, security.azauthorizationstore_delegatedpolicyusers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::get_DelegatedPolicyUsers


## -description


The <b>DelegatedPolicyUsers</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) of principals that act as delegated policy users in text form.

This property is read-only.


## -parameters


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>  or <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
In  JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



