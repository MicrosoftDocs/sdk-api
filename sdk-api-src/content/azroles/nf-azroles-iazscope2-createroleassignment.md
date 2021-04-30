---
UID: NF:azroles.IAzScope2.CreateRoleAssignment
title: IAzScope2::CreateRoleAssignment (azroles.h)
description: Creates a new IAzRoleAssignment object with the specified name in this scope.
helpviewer_keywords: ["CreateRoleAssignment","CreateRoleAssignment method [Security]","CreateRoleAssignment method [Security]","IAzScope2 interface","IAzScope2 interface [Security]","CreateRoleAssignment method","IAzScope2.CreateRoleAssignment","IAzScope2::CreateRoleAssignment","azroles/IAzScope2::CreateRoleAssignment","security.iazscope2_createroleassignment"]
old-location: security\iazscope2_createroleassignment.htm
tech.root: security
ms.assetid: 98cb412b-9742-4f94-a470-61e675f6b253
ms.date: 12/05/2018
ms.keywords: CreateRoleAssignment, CreateRoleAssignment method [Security], CreateRoleAssignment method [Security],IAzScope2 interface, IAzScope2 interface [Security],CreateRoleAssignment method, IAzScope2.CreateRoleAssignment, IAzScope2::CreateRoleAssignment, azroles/IAzScope2::CreateRoleAssignment, security.iazscope2_createroleassignment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzScope2::CreateRoleAssignment
 - azroles/IAzScope2::CreateRoleAssignment
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
 - IAzScope2.CreateRoleAssignment
---

# IAzScope2::CreateRoleAssignment


## -description

The <b>CreateRoleAssignment</b> method creates a new <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object with the specified name in this scope.

## -parameters

### -param bstrRoleAssignmentName [in]

A string that contains the name of the new <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object.

### -param ppRoleAssignment [out]

The address of  a pointer to the <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object that this method creates.

When you have finished using the <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.