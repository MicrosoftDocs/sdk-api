---
UID: NF:azroles.IAzApplication.get_PolicyReadersName
title: IAzApplication::get_PolicyReadersName
author: windows-sdk-content
description: The IAzApplication::PolicyReadersName property retrieves the account names of principals that act as policy readers.
old-location: security\iazapplication_policyreadersname.htm
tech.root: secauthz
ms.assetid: e6ed4504-0df1-438b-87c7-1861264d02bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzApplication object [Security],PolicyReadersName property, IAzApplication interface [Security],PolicyReadersName property, IAzApplication.PolicyReadersName, IAzApplication.get_PolicyReadersName, IAzApplication::PolicyReadersName, IAzApplication::get_PolicyReadersName, PolicyReadersName property [Security], PolicyReadersName property [Security],AzApplication object, PolicyReadersName property [Security],IAzApplication interface, azroles/IAzApplication::PolicyReadersName, azroles/IAzApplication::get_PolicyReadersName, get_PolicyReadersName, security.iazapplication_policyreadersname
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
 - IAzApplication.PolicyReadersName
 - IAzApplication.get_PolicyReadersName
 - AzApplication.PolicyReadersName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_PolicyReadersName


## -description


The <b>PolicyReadersName</b> property retrieves the account names of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



