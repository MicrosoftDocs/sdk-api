---
UID: NF:azroles.IAzRole.AddAppMember
title: IAzRole::AddAppMember
author: windows-sdk-content
description: Adds the specified IAzApplicationGroup object to the list of application groups that belong to this role.
old-location: security\iazrole_addappmember.htm
old-project: SecAuthZ
ms.assetid: 118387f8-a422-4a8d-9d12-a5b5ee1e7b06
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: AddAppMember, AddAppMember method [Security], AddAppMember method [Security],AzRole object, AddAppMember method [Security],IAzRole interface, AzRole object [Security],AddAppMember method, IAzRole interface [Security],AddAppMember method, IAzRole.AddAppMember, IAzRole::AddAppMember, azroles/IAzRole::AddAppMember, security.iazrole_addappmember
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IAzRole.AddAppMember
 - AzRole.AddAppMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::AddAppMember


## -description


The <b>AddAppMember</b> method adds the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to the list of application groups that belong to this role.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to add to the list of the application groups that belong to this role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that belong to this role, use the <a href="https://msdn.microsoft.com/c41933d4-d3fe-485c-9249-e82d51c0bfc9">AppMembers</a> property.

You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



