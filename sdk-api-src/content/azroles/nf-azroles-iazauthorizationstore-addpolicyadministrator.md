---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyAdministrator
title: IAzAuthorizationStore::AddPolicyAdministrator (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy administrators. (IAzAuthorizationStore.AddPolicyAdministrator)
helpviewer_keywords: ["AddPolicyAdministrator","AddPolicyAdministrator method [Security]","AddPolicyAdministrator method [Security]","AzAuthorizationStore object","AddPolicyAdministrator method [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","AddPolicyAdministrator method","IAzAuthorizationStore interface [Security]","AddPolicyAdministrator method","IAzAuthorizationStore.AddPolicyAdministrator","IAzAuthorizationStore::AddPolicyAdministrator","azroles/IAzAuthorizationStore::AddPolicyAdministrator","security.azauthorizationstore_addpolicyadministrator"]
old-location: security\azauthorizationstore_addpolicyadministrator.htm
tech.root: security
ms.assetid: 8d73bc05-1366-4b47-9eaf-4a247ebf8d93
ms.date: 03/20/2023
ms.keywords: AddPolicyAdministrator, AddPolicyAdministrator method [Security], AddPolicyAdministrator method [Security],AzAuthorizationStore object, AddPolicyAdministrator method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyAdministrator method, IAzAuthorizationStore interface [Security],AddPolicyAdministrator method, IAzAuthorizationStore.AddPolicyAdministrator, IAzAuthorizationStore::AddPolicyAdministrator, azroles/IAzAuthorizationStore::AddPolicyAdministrator, security.azauthorizationstore_addpolicyadministrator
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
 - IAzAuthorizationStore::AddPolicyAdministrator
 - azroles/IAzAuthorizationStore::AddPolicyAdministrator
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
 - AzAuthorizationStore.AddPolicyAdministrator
 - IAzAuthorizationStore.AddPolicyAdministrator
---

# IAzAuthorizationStore::AddPolicyAdministrator

## -description

The **AddPolicyAdministrator** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form to the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Text form of the SID to add to the list of policy administrators.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy administrators for an object can perform the following tasks:

- Read the object
- Write attributes to the object
- Read attributes of child objects of the object
- Write attributes to child objects of the object
- Delete the object
- Delete child objects of the object
- Create child objects of the object

To view the list of policy administrators, use the [PolicyAdministrators](nf-azroles-iazauthorizationstore-get_policyadministrators.md) property.

You must call the [Submit](nf-azroles-iazauthorizationstore-submit.md) method to persist any changes made by this method.

## -see-also

[PolicyAdministrators](nf-azroles-iazauthorizationstore-get_policyadministrators.md)
