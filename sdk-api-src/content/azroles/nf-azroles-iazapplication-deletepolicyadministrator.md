---
UID: NF:azroles.IAzApplication.DeletePolicyAdministrator
title: IAzApplication::DeletePolicyAdministrator (azroles.h)
description: The DeletePolicyAdministrator method of IAzApplication removes the specified security identifier in text form from the list of principals that act as policy administrators.
helpviewer_keywords: ["AzApplication object [Security]","DeletePolicyAdministrator method","DeletePolicyAdministrator","DeletePolicyAdministrator method [Security]","DeletePolicyAdministrator method [Security]","AzApplication object","DeletePolicyAdministrator method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeletePolicyAdministrator method","IAzApplication.DeletePolicyAdministrator","IAzApplication::DeletePolicyAdministrator","azroles/IAzApplication::DeletePolicyAdministrator","security.iazapplication_deletepolicyadministrator"]
old-location: security\iazapplication_deletepolicyadministrator.htm
tech.root: security
ms.assetid: 240dbfbc-ae0f-4a8e-9cbc-b58efb258ad5
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeletePolicyAdministrator method, DeletePolicyAdministrator, DeletePolicyAdministrator method [Security], DeletePolicyAdministrator method [Security],AzApplication object, DeletePolicyAdministrator method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyAdministrator method, IAzApplication.DeletePolicyAdministrator, IAzApplication::DeletePolicyAdministrator, azroles/IAzApplication::DeletePolicyAdministrator, security.iazapplication_deletepolicyadministrator
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
 - IAzApplication::DeletePolicyAdministrator
 - azroles/IAzApplication::DeletePolicyAdministrator
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
 - IAzApplication.DeletePolicyAdministrator
 - AzApplication.DeletePolicyAdministrator
---

# IAzApplication::DeletePolicyAdministrator

## -description

The **DeletePolicyAdministrator** method removes the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Text form of the SID to remove from the list of policy administrators.

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

To view the list of policy administrators, use the [PolicyAdministrators](nf-azroles-iazapplication-get_policyadministrators.md) property.

## -see-also

[PolicyAdministrators](nf-azroles-iazapplication-get_policyadministrators.md)
