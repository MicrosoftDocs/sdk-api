---
UID: NF:azroles.IAzAuthorizationStore.get_PolicyReadersName
title: IAzAuthorizationStore::get_PolicyReadersName
author: windows-sdk-content
description: Retrieves the account names of principals that act as policy readers.
old-location: security\azauthorizationstore_policyreadersname.htm
old-project: SecAuthZ
ms.assetid: d550448e-a1ea-45f3-9151-affd4b8c0b14
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzAuthorizationStore object [Security],PolicyReadersName property, IAzAuthorizationStore interface [Security],PolicyReadersName property, IAzAuthorizationStore.PolicyReadersName, IAzAuthorizationStore.get_PolicyReadersName, IAzAuthorizationStore::PolicyReadersName, IAzAuthorizationStore::get_PolicyReadersName, PolicyReadersName property [Security], PolicyReadersName property [Security],AzAuthorizationStore object, PolicyReadersName property [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::PolicyReadersName, azroles/IAzAuthorizationStore::get_PolicyReadersName, get_PolicyReadersName, security.azauthorizationstore_policyreadersname
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
-	IAzAuthorizationStore.PolicyReadersName
-	IAzAuthorizationStore.get_PolicyReadersName
-	AzAuthorizationStore.PolicyReadersName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::get_PolicyReadersName


## -description


The <b>PolicyReadersName</b> property retrieves the account names of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In  JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



