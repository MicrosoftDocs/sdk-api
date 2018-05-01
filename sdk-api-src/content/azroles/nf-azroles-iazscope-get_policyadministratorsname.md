---
UID: NF:azroles.IAzScope.get_PolicyAdministratorsName
title: IAzScope::get_PolicyAdministratorsName method
author: windows-driver-content
description: Retrieves the account names of principals that act as policy administrators.
old-location: security\iazscope_policyadministratorsname.htm
old-project: SecAuthZ
ms.assetid: 291aa2f8-f08e-45f5-ade7-b456c962dd3f
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzScope object [Security], PolicyAdministratorsName property, IAzScope, IAzScope interface [Security], PolicyAdministratorsName property, IAzScope.PolicyAdministratorsName, IAzScope::get_PolicyAdministratorsName, PolicyAdministratorsName property [Security], PolicyAdministratorsName property [Security], AzScope object, PolicyAdministratorsName property [Security], IAzScope interface, azroles/IAzScope::PolicyAdministratorsName, azroles/IAzScope::get_PolicyAdministratorsName, get_PolicyAdministratorsName,IAzScope.get_PolicyAdministratorsName, security.iazscope_policyadministratorsname
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
-	IAzScope.PolicyAdministratorsName
-	IAzScope.get_PolicyAdministratorsName
-	AzScope.PolicyAdministratorsName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::get_PolicyAdministratorsName method


## -description


The <b>PolicyAdministratorsName</b> property retrieves the account names of principals that act as policy administrators.

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



