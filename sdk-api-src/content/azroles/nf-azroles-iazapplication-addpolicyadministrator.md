---
UID: NF:azroles.IAzApplication.AddPolicyAdministrator
title: IAzApplication::AddPolicyAdministrator
author: windows-driver-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy administrators.
old-location: security\iazapplication_addpolicyadministrator.htm
old-project: SecAuthZ
ms.assetid: 944f93c1-5155-4c87-a241-9fdef84b68fc
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AddPolicyAdministrator, AddPolicyAdministrator method [Security], AddPolicyAdministrator method [Security],AzApplication object, AddPolicyAdministrator method [Security],IAzApplication interface, AzApplication object [Security],AddPolicyAdministrator method, IAzApplication interface [Security],AddPolicyAdministrator method, IAzApplication.AddPolicyAdministrator, IAzApplication::AddPolicyAdministrator, azroles/IAzApplication::AddPolicyAdministrator, security.iazapplication_addpolicyadministrator
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication.AddPolicyAdministrator
-	AzApplication.AddPolicyAdministrator
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::AddPolicyAdministrator


## -description


The <b>AddPolicyAdministrator</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.


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
To view the list of policy administrators, use the <a href="https://msdn.microsoft.com/a0b66213-3dc7-4886-9c93-0d27d43a7d92">PolicyAdministrators</a> property.

You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



