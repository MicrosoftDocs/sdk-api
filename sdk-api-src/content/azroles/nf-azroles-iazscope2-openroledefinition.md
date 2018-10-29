---
UID: NF:azroles.IAzScope2.OpenRoleDefinition
title: IAzScope2::OpenRoleDefinition
author: windows-sdk-content
description: Opens an IAzRoleDefinition object with the specified name in this scope.
old-location: security\iazscope2_openroledefinition.htm
tech.root: SecAuthZ
ms.assetid: 58b792aa-1432-4b23-8d7a-33606741bf27
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAzScope2 interface [Security],OpenRoleDefinition method, IAzScope2.OpenRoleDefinition, IAzScope2::OpenRoleDefinition, OpenRoleDefinition, OpenRoleDefinition method [Security], OpenRoleDefinition method [Security],IAzScope2 interface, azroles/IAzScope2::OpenRoleDefinition, security.iazscope2_openroledefinition
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzScope2.OpenRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzScope2::OpenRoleDefinition


## -description


The <b>OpenRoleDefinition</b> method opens an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name in this scope.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to open.


### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object that this method opens.

When you have finished using the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object, release it by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



