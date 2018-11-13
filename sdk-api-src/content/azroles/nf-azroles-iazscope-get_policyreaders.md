---
UID: NF:azroles.IAzScope.get_PolicyReaders
title: IAzScope::get_PolicyReaders
author: windows-sdk-content
description: The PolicyReaders property of IAzScope retrieves the security identifiers (SIDs), in text form, of principals that act as policy readers.
old-location: security\iazscope_policyreaders.htm
tech.root: SecAuthZ
ms.assetid: 7576997c-a585-4f0d-bec5-c616d39633f9
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AzScope object [Security],PolicyReaders property, IAzScope interface [Security],PolicyReaders property, IAzScope.PolicyReaders, IAzScope.get_PolicyReaders, IAzScope::PolicyReaders, IAzScope::get_PolicyReaders, PolicyReaders property [Security], PolicyReaders property [Security],AzScope object, PolicyReaders property [Security],IAzScope interface, azroles/IAzScope::PolicyReaders, azroles/IAzScope::get_PolicyReaders, get_PolicyReaders, security.iazscope_policyreaders
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
 - IAzScope.PolicyReaders
 - IAzScope.get_PolicyReaders
 - AzScope.PolicyReaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::get_PolicyReaders


## -description


The <b>PolicyReaders</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



