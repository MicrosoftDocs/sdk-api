---
UID: NF:azroles.IAzScope.DeletePolicyAdministrator
title: IAzScope::DeletePolicyAdministrator
author: windows-sdk-content
description: The DeletePolicyAdministrator method of IAzScope removes the specified security identifier in text form from the list of principals that act as policy administrators.
old-location: security\iazscope_deletepolicyadministrator.htm
old-project: secauthz
ms.assetid: 23077da5-5475-45c6-87c0-b38f6c05d386
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzScope object [Security],DeletePolicyAdministrator method, DeletePolicyAdministrator, DeletePolicyAdministrator method [Security], DeletePolicyAdministrator method [Security],AzScope object, DeletePolicyAdministrator method [Security],IAzScope interface, IAzScope interface [Security],DeletePolicyAdministrator method, IAzScope.DeletePolicyAdministrator, IAzScope::DeletePolicyAdministrator, azroles/IAzScope::DeletePolicyAdministrator, security.iazscope_deletepolicyadministrator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - IAzScope.DeletePolicyAdministrator
 - AzScope.DeletePolicyAdministrator
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::DeletePolicyAdministrator


## -description


The <b>DeletePolicyAdministrator</b> method removes the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of principals that act as policy administrators.


## -parameters




### -param bstrAdmin [in]

Text form of the SID to remove from the list of policy administrators.


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



