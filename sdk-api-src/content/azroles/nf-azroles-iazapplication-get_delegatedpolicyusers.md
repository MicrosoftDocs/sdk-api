---
UID: NF:azroles.IAzApplication.get_DelegatedPolicyUsers
title: IAzApplication::get_DelegatedPolicyUsers
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs), in text form, of principals that act as delegated policy users.
old-location: security\iazapplication_delegatedpolicyusers.htm
tech.root: SecAuthZ
ms.assetid: b20e1d5c-b07e-4f75-8b63-38036b07b24d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzApplication object [Security],DelegatedPolicyUsers property, DelegatedPolicyUsers property [Security], DelegatedPolicyUsers property [Security],AzApplication object, DelegatedPolicyUsers property [Security],IAzApplication interface, IAzApplication interface [Security],DelegatedPolicyUsers property, IAzApplication.DelegatedPolicyUsers, IAzApplication.get_DelegatedPolicyUsers, IAzApplication::DelegatedPolicyUsers, IAzApplication::get_DelegatedPolicyUsers, azroles/IAzApplication::DelegatedPolicyUsers, azroles/IAzApplication::get_DelegatedPolicyUsers, get_DelegatedPolicyUsers, security.iazapplication_delegatedpolicyusers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_DelegatedPolicyUsers


## -description


The <b>DelegatedPolicyUsers</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of principals that act as delegated policy users.

This property is read-only.


## -parameters


## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
In JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



