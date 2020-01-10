---
UID: NF:azroles.IAzRoleAssignment.AddRoleDefinition
title: IAzRoleAssignment::AddRoleDefinition (azroles.h)
description: Adds the specified IAzRoleDefinition object to this IAzRoleAssignment object.
old-location: security\iazroleassignment_addroledefinition.htm
tech.root: SecAuthZ
ms.assetid: 9946d273-3726-40f4-b438-7f2377fc8013
ms.date: 12/05/2018
ms.keywords: AddRoleDefinition, AddRoleDefinition method [Security], AddRoleDefinition method [Security],IAzRoleAssignment interface, IAzRoleAssignment interface [Security],AddRoleDefinition method, IAzRoleAssignment.AddRoleDefinition, IAzRoleAssignment::AddRoleDefinition, azroles/IAzRoleAssignment::AddRoleDefinition, security.iazroleassignment_addroledefinition
f1_keywords:
- azroles/IAzRoleAssignment.AddRoleDefinition
dev_langs:
- c++
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
- IAzRoleAssignment.AddRoleDefinition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzRoleAssignment::AddRoleDefinition


## -description


The <b>AddRoleDefinition</b> method adds the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to this <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object.


## -parameters




### -param bstrRoleDefinition [in]

The name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> to add.


## -returns



If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.



