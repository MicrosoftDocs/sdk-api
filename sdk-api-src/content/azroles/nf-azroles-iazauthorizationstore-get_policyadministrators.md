---
UID: NF:azroles.IAzAuthorizationStore.get_PolicyAdministrators
title: IAzAuthorizationStore::get_PolicyAdministrators
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs) of principals that act as policy administrators in text form.
old-location: security\azauthorizationstore_policyadministrators.htm
old-project: SecAuthZ
ms.assetid: 388d4970-5de4-4216-8c26-b9b24cc82ca3
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzAuthorizationStore object [Security],PolicyAdministrators property, IAzAuthorizationStore interface [Security],PolicyAdministrators property, IAzAuthorizationStore.PolicyAdministrators, IAzAuthorizationStore.get_PolicyAdministrators, IAzAuthorizationStore::PolicyAdministrators, IAzAuthorizationStore::get_PolicyAdministrators, PolicyAdministrators property [Security], PolicyAdministrators property [Security],AzAuthorizationStore object, PolicyAdministrators property [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::PolicyAdministrators, azroles/IAzAuthorizationStore::get_PolicyAdministrators, get_PolicyAdministrators, security.azauthorizationstore_policyadministrators
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzAuthorizationStore.PolicyAdministrators
-	IAzAuthorizationStore.get_PolicyAdministrators
-	AzAuthorizationStore.PolicyAdministrators
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::get_PolicyAdministrators


## -description


The <b>PolicyAdministrators</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) of principals that act as policy administrators in text form.

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
In  JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



