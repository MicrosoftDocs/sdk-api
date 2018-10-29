---
UID: NF:azroles.IAzRole.AddAppMember
title: IAzRole::AddAppMember
author: windows-sdk-content
description: Adds the specified IAzApplicationGroup object to the list of application groups that belong to this role.
old-location: security\iazrole_addappmember.htm
tech.root: SecAuthZ
ms.assetid: 118387f8-a422-4a8d-9d12-a5b5ee1e7b06
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddAppMember, AddAppMember method [Security], AddAppMember method [Security],AzRole object, AddAppMember method [Security],IAzRole interface, AzRole object [Security],AddAppMember method, IAzRole interface [Security],AddAppMember method, IAzRole.AddAppMember, IAzRole::AddAppMember, azroles/IAzRole::AddAppMember, security.iazrole_addappmember
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Azroles.lib
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
 - IAzRole.AddAppMember
 - AzRole.AddAppMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzRole::AddAppMember


## -description


The <b>AddAppMember</b> method adds the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object to the list of application groups that belong to this role.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://msdn.microsoft.com/en-us/library/Aa377318(v=VS.85).aspx">Name</a> property of the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object to add to the list of the application groups that belong to this role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that belong to this role, use the <a href="https://msdn.microsoft.com/en-us/library/Aa378176(v=VS.85).aspx">AppMembers</a> property.

You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa378231(v=VS.85).aspx">Submit</a> method to persist any changes made by this method.



