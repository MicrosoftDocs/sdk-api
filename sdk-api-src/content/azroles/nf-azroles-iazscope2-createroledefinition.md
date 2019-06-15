---
UID: NF:azroles.IAzScope2.CreateRoleDefinition
title: IAzScope2::CreateRoleDefinition (azroles.h)
author: windows-sdk-content
description: Creates a new IAzRoleDefinition object with the specified name in this scope.
old-location: security\iazscope2_createroledefinition.htm
tech.root: SecAuthZ
ms.assetid: bcd78233-a484-4c99-9dbb-9f559f7542a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateRoleDefinition, CreateRoleDefinition method [Security], CreateRoleDefinition method [Security],IAzScope2 interface, IAzScope2 interface [Security],CreateRoleDefinition method, IAzScope2.CreateRoleDefinition, IAzScope2::CreateRoleDefinition, azroles/IAzScope2::CreateRoleDefinition, security.iazscope2_createroledefinition
ms.topic: method
f1_keywords: ["azroles/IAzScope2.CreateRoleDefinition"]
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
 - IAzScope2.CreateRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzScope2::CreateRoleDefinition


## -description


The <b>CreateRoleDefinition</b> method creates a new <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name in this scope.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the new <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object.


### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object that this method creates.

When you have finished using the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object, release it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



