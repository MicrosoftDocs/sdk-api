---
UID: NF:azroles.IAzScope.AddPolicyAdministrator
title: IAzScope::AddPolicyAdministrator
author: windows-sdk-content
description: The AddPolicyAdministrator method of IAzScope adds the specified security identifier in text form to the list of principals that act as policy administrators.
old-location: security\iazscope_addpolicyadministrator.htm
tech.root: SecAuthZ
ms.assetid: 7aa77615-1f12-4641-877e-87b26343db4d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddPolicyAdministrator, AddPolicyAdministrator method [Security], AddPolicyAdministrator method [Security],AzScope object, AddPolicyAdministrator method [Security],IAzScope interface, AzScope object [Security],AddPolicyAdministrator method, IAzScope interface [Security],AddPolicyAdministrator method, IAzScope.AddPolicyAdministrator, IAzScope::AddPolicyAdministrator, azroles/IAzScope::AddPolicyAdministrator, security.iazscope_addpolicyadministrator
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
 - IAzScope.AddPolicyAdministrator
 - AzScope.AddPolicyAdministrator
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzScope.AddPolicyAdministrator
: 
---

# IAzScope::AddPolicyAdministrator


## -description


The <b>AddPolicyAdministrator</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form  to the list of principals that act as policy administrators.


## -parameters




### -param bstrAdmin [in]

Text form of the SID to add to the list of policy administrators.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
To view the list of policy administrators, use the <a href="https://msdn.microsoft.com/13c11105-b44d-46e0-ab73-c11fede1507b">PolicyAdministrators</a> property.

You must call the <a href="https://msdn.microsoft.com/c06f1994-71d9-4867-a5ed-8fa90206994f">Submit</a> method to persist any changes made by this method.



