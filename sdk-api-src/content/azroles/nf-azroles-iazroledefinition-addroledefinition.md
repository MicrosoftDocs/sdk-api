---
UID: NF:azroles.IAzRoleDefinition.AddRoleDefinition
title: IAzRoleDefinition::AddRoleDefinition
author: windows-sdk-content
description: Adds the specified IAzRoleDefinition object to this IAzRoleDefinition object.
old-location: security\iazroledefinition_addroledefinition.htm
tech.root: secauthz
ms.assetid: 38d65f5f-452b-4641-a683-2740fb529064
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddRoleDefinition, AddRoleDefinition method [Security], AddRoleDefinition method [Security],IAzRoleDefinition interface, IAzRoleDefinition interface [Security],AddRoleDefinition method, IAzRoleDefinition.AddRoleDefinition, IAzRoleDefinition::AddRoleDefinition, azroles/IAzRoleDefinition::AddRoleDefinition, security.iazroledefinition_addroledefinition
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
 - IAzRoleDefinition.AddRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzRoleDefinition::AddRoleDefinition


## -description


The <b>AddRoleDefinition</b> method adds the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to this <b>IAzRoleDefinition</b> object.


## -parameters




### -param bstrRoleDefinition [in]

The name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> to add.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a> method to persist any changes made by this method.



