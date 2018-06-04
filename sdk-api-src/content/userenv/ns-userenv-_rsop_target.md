---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _RSOP_TARGET structure


## -description


The
    <b>RSOP_TARGET</b> structure contains computer and user information required by the 
<a href="https://msdn.microsoft.com/748b61a1-79fb-44b9-8c9b-0b1746fa981b">GenerateGroupPolicy</a> function.


## -struct-fields




### -field pwszAccountName

Pointer to the account name of the computer or the user.


### -field pwszNewSOM

Pointer to the new domain or organizational unit that is the location for the account identified by the <b>pwszAccountName</b> member. This member can be <b>NULL</b>.


### -field psaSecurityGroups

Pointer to a <b>SAFEARRAY</b> that contains a proposed list of new security groups. This member can be <b>NULL</b>. For more information about security groups, see 
<a href="https://msdn.microsoft.com/eb552416-0cf0-4510-b1f8-082e1506370e">Filtering the Scope of a GPO</a> and 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a>.


### -field pRsopToken

Pointer to an <b>RSOPTOKEN</b> to use with the 
<a href="https://msdn.microsoft.com/d63734a0-1a88-4669-828e-de467606fc14">RSoPAccessCheckByType</a> and the 
<a href="https://msdn.microsoft.com/dfdf14ee-fee1-4e96-9955-7f24dfe39487">RSoPFileAccessCheck</a> functions.


### -field pGPOList

Pointer to a 
<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a> structure containing a linked list of GPOs.


### -field pWbemServices

Specifies the WMI services pointer to the namespace to which the planning mode policy data should be written.


## -see-also




<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>



<a href="https://msdn.microsoft.com/748b61a1-79fb-44b9-8c9b-0b1746fa981b">GenerateGroupPolicy</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/d63734a0-1a88-4669-828e-de467606fc14">RSoPAccessCheckByType</a>



<a href="https://msdn.microsoft.com/dfdf14ee-fee1-4e96-9955-7f24dfe39487">RSoPFileAccessCheck</a>
 

 

