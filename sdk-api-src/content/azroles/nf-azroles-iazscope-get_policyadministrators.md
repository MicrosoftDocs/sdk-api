---
UID: NF:azroles.IAzScope.get_PolicyAdministrators
title: IAzScope::get_PolicyAdministrators
author: windows-sdk-content
description: The PolicyAdministrators property of IAzScope retrieves the security identifiers (SIDs), in text form, of principals that act as policy administrators.
old-location: security\iazscope_policyadministrators.htm
tech.root: SecAuthZ
ms.assetid: 13c11105-b44d-46e0-ab73-c11fede1507b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AzScope object [Security],PolicyAdministrators property, IAzScope interface [Security],PolicyAdministrators property, IAzScope.PolicyAdministrators, IAzScope.get_PolicyAdministrators, IAzScope::PolicyAdministrators, IAzScope::get_PolicyAdministrators, PolicyAdministrators property [Security], PolicyAdministrators property [Security],AzScope object, PolicyAdministrators property [Security],IAzScope interface, azroles/IAzScope::PolicyAdministrators, azroles/IAzScope::get_PolicyAdministrators, get_PolicyAdministrators, security.iazscope_policyadministrators
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
 - IAzScope.PolicyAdministrators
 - IAzScope.get_PolicyAdministrators
 - AzScope.PolicyAdministrators
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
- IAzScope.get_PolicyAdministrators
: 
---

# IAzScope::get_PolicyAdministrators


## -description


The <b>PolicyAdministrators</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of principals that act as policy administrators.

This property is read-only.


## -parameters


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
In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



