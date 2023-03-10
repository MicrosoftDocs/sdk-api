---
UID: NF:azroles.IAzApplication.AddPolicyAdministrator
title: IAzApplication::AddPolicyAdministrator (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy administrators. (IAzApplication.AddPolicyAdministrator)
helpviewer_keywords: ["AddPolicyAdministrator","AddPolicyAdministrator method [Security]","AddPolicyAdministrator method [Security]","AzApplication object","AddPolicyAdministrator method [Security]","IAzApplication interface","AzApplication object [Security]","AddPolicyAdministrator method","IAzApplication interface [Security]","AddPolicyAdministrator method","IAzApplication.AddPolicyAdministrator","IAzApplication::AddPolicyAdministrator","azroles/IAzApplication::AddPolicyAdministrator","security.iazapplication_addpolicyadministrator"]
old-location: security\iazapplication_addpolicyadministrator.htm
tech.root: security
ms.assetid: 944f93c1-5155-4c87-a241-9fdef84b68fc
ms.date: 12/05/2018
ms.keywords: AddPolicyAdministrator, AddPolicyAdministrator method [Security], AddPolicyAdministrator method [Security],AzApplication object, AddPolicyAdministrator method [Security],IAzApplication interface, AzApplication object [Security],AddPolicyAdministrator method, IAzApplication interface [Security],AddPolicyAdministrator method, IAzApplication.AddPolicyAdministrator, IAzApplication::AddPolicyAdministrator, azroles/IAzApplication::AddPolicyAdministrator, security.iazapplication_addpolicyadministrator
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
 - IAzApplication::AddPolicyAdministrator
 - azroles/IAzApplication::AddPolicyAdministrator
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
 - IAzApplication.AddPolicyAdministrator
 - AzApplication.AddPolicyAdministrator
---

# IAzApplication::AddPolicyAdministrator


## -description

The <b>AddPolicyAdministrator</b> method adds the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Text form of the SID to add to the list of policy administrators.

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
To view the list of policy administrators, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministrators">PolicyAdministrators</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.
