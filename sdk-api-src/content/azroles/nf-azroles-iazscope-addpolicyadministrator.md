---
UID: NF:azroles.IAzScope.AddPolicyAdministrator
title: IAzScope::AddPolicyAdministrator (azroles.h)
description: The AddPolicyAdministrator method of IAzScope adds the specified security identifier in text form to the list of principals that act as policy administrators.
helpviewer_keywords: ["AddPolicyAdministrator","AddPolicyAdministrator method [Security]","AddPolicyAdministrator method [Security]","AzScope object","AddPolicyAdministrator method [Security]","IAzScope interface","AzScope object [Security]","AddPolicyAdministrator method","IAzScope interface [Security]","AddPolicyAdministrator method","IAzScope.AddPolicyAdministrator","IAzScope::AddPolicyAdministrator","azroles/IAzScope::AddPolicyAdministrator","security.iazscope_addpolicyadministrator"]
old-location: security\iazscope_addpolicyadministrator.htm
tech.root: security
ms.assetid: 7aa77615-1f12-4641-877e-87b26343db4d
ms.date: 03/20/2023
ms.keywords: AddPolicyAdministrator, AddPolicyAdministrator method [Security], AddPolicyAdministrator method [Security],AzScope object, AddPolicyAdministrator method [Security],IAzScope interface, AzScope object [Security],AddPolicyAdministrator method, IAzScope interface [Security],AddPolicyAdministrator method, IAzScope.AddPolicyAdministrator, IAzScope::AddPolicyAdministrator, azroles/IAzScope::AddPolicyAdministrator, security.iazscope_addpolicyadministrator
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
 - IAzScope::AddPolicyAdministrator
 - azroles/IAzScope::AddPolicyAdministrator
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
 - IAzScope.AddPolicyAdministrator
 - AzScope.AddPolicyAdministrator
---

# IAzScope::AddPolicyAdministrator

## -description

The **AddPolicyAdministrator** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form  to the list of principals that act as policy administrators.

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

To view the list of policy administrators, use the [PolicyAdministrators](nf-azroles-iazscope-get_policyadministrators.md) property.

You must call the [Submit](nf-azroles-iazscope-submit.md) method to persist any changes made by this method.

## -see-also

[PolicyAdministrators](nf-azroles-iazscope-get_policyadministrators.md)

[Submit](nf-azroles-iazscope-submit.md)
