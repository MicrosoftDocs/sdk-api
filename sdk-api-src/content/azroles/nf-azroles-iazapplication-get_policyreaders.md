---
UID: NF:azroles.IAzApplication.get_PolicyReaders
title: IAzApplication::get_PolicyReaders
author: windows-sdk-content
description: Retrieves the security identifiers (SIDs), in text form, of principals that act as policy readers.
old-location: security\iazapplication_policyreaders.htm
tech.root: secauthz
ms.assetid: 7dcacc91-6327-4e6c-8aa0-06e7e0191a41
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AzApplication object [Security],PolicyReaders property, IAzApplication interface [Security],PolicyReaders property, IAzApplication.PolicyReaders, IAzApplication.get_PolicyReaders, IAzApplication::PolicyReaders, IAzApplication::get_PolicyReaders, PolicyReaders property [Security], PolicyReaders property [Security],AzApplication object, PolicyReaders property [Security],IAzApplication interface, azroles/IAzApplication::PolicyReaders, azroles/IAzApplication::get_PolicyReaders, get_PolicyReaders, security.iazapplication_policyreaders
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
 - IAzApplication.PolicyReaders
 - IAzApplication.get_PolicyReaders
 - AzApplication.PolicyReaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_PolicyReaders


## -description


The <b>PolicyReaders</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs), in text form, of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



