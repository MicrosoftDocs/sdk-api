---
UID: NF:azroles.IAzApplication.get_PolicyReaders
title: IAzApplication::get_PolicyReaders
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs), in text form, of principals that act as policy readers.
old-location: security\iazapplication_policyreaders.htm
old-project: SecAuthZ
ms.assetid: 7dcacc91-6327-4e6c-8aa0-06e7e0191a41
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzApplication object [Security],PolicyReaders property, IAzApplication interface [Security],PolicyReaders property, IAzApplication.PolicyReaders, IAzApplication.get_PolicyReaders, IAzApplication::PolicyReaders, IAzApplication::get_PolicyReaders, PolicyReaders property [Security], PolicyReaders property [Security],AzApplication object, PolicyReaders property [Security],IAzApplication interface, azroles/IAzApplication::PolicyReaders, azroles/IAzApplication::get_PolicyReaders, get_PolicyReaders, security.iazapplication_policyreaders
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
-	IAzApplication.PolicyReaders
-	IAzApplication.get_PolicyReaders
-	AzApplication.PolicyReaders
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::get_PolicyReaders


## -description


The <b>PolicyReaders</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



