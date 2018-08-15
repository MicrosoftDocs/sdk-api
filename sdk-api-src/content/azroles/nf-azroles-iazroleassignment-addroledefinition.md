---
UID: NF:azroles.IAzRoleAssignment.AddRoleDefinition
title: IAzRoleAssignment::AddRoleDefinition
author: windows-sdk-content
description: Adds the specified IAzRoleDefinition object to this IAzRoleAssignment object.
old-location: security\iazroleassignment_addroledefinition.htm
old-project: secauthz
ms.assetid: 9946d273-3726-40f4-b438-7f2377fc8013
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddRoleDefinition, AddRoleDefinition method [Security], AddRoleDefinition method [Security],IAzRoleAssignment interface, IAzRoleAssignment interface [Security],AddRoleDefinition method, IAzRoleAssignment.AddRoleDefinition, IAzRoleAssignment::AddRoleDefinition, azroles/IAzRoleAssignment::AddRoleDefinition, security.iazroleassignment_addroledefinition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
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
 - IAzRoleAssignment.AddRoleDefinition
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzRoleAssignment::AddRoleDefinition


## -description


The <b>AddRoleDefinition</b> method adds the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to this <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object.


## -parameters




### -param bstrRoleDefinition [in]

The name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> to add.


## -returns



If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



