---
UID: NF:azroles.IAzScope.get_PolicyReadersName
title: IAzScope::get_PolicyReadersName
author: windows-sdk-content
description: Retrieves the account names of principals that act as policy readers.
old-location: security\iazscope_policyreadersname.htm
tech.root: SecAuthZ
ms.assetid: 4f56ee3f-f987-4569-9e19-c13ab3ff100a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzScope object [Security],PolicyReadersName property, IAzScope interface [Security],PolicyReadersName property, IAzScope.PolicyReadersName, IAzScope.get_PolicyReadersName, IAzScope::PolicyReadersName, IAzScope::get_PolicyReadersName, PolicyReadersName property [Security], PolicyReadersName property [Security],AzScope object, PolicyReadersName property [Security],IAzScope interface, azroles/IAzScope::PolicyReadersName, azroles/IAzScope::get_PolicyReadersName, get_PolicyReadersName, security.iazscope_policyreadersname
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
 - IAzScope.PolicyReadersName
 - IAzScope.get_PolicyReadersName
 - AzScope.PolicyReadersName
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::get_PolicyReadersName


## -description


The <b>PolicyReadersName</b> property retrieves the account names of principals that act as policy readers.

This property is read-only.


## -parameters


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="https://msdn.microsoft.com/en-us/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="https://msdn.microsoft.com/library/k4h76zbx(v=VS.85).aspx">Array</a> object. 



