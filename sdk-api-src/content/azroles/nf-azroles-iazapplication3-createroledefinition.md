---
UID: NF:azroles.IAzApplication3.CreateRoleDefinition
title: IAzApplication3::CreateRoleDefinition
author: windows-sdk-content
description: Creates a new IAzRoleDefinition object with the specified name.
old-location: security\iazapplication3_createroledefinition.htm
old-project: SecAuthZ
ms.assetid: 014410be-4b2c-452b-b671-0a9bd9c0a448
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CreateRoleDefinition, CreateRoleDefinition method [Security], CreateRoleDefinition method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],CreateRoleDefinition method, IAzApplication3.CreateRoleDefinition, IAzApplication3::CreateRoleDefinition, azroles/IAzApplication3::CreateRoleDefinition, security.iazapplication3_createroledefinition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IAzApplication3.CreateRoleDefinition
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3::CreateRoleDefinition


## -description


The <b>CreateRoleDefinition</b> method creates a new <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the new <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object.


### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object that this method creates.

When you have finished using this <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object, release it by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



