---
UID: NF:azroles.IAzApplication.DeletePolicyReader
title: IAzApplication::DeletePolicyReader
author: windows-sdk-content
description: The DeletePolicyReader method of IAzApplication removes the specified security identifier in text form from the list of principals that act as policy readers.
old-location: security\iazapplication_deletepolicyreader.htm
old-project: secauthz
ms.assetid: aec8b5c4-3c5e-4b91-a10f-40ef05beca1f
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzApplication object [Security],DeletePolicyReader method, DeletePolicyReader, DeletePolicyReader method [Security], DeletePolicyReader method [Security],AzApplication object, DeletePolicyReader method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyReader method, IAzApplication.DeletePolicyReader, IAzApplication::DeletePolicyReader, azroles/IAzApplication::DeletePolicyReader, security.iazapplication_deletepolicyreader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.DeletePolicyReader
 - AzApplication.DeletePolicyReader
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::DeletePolicyReader


## -description


The <b>DeletePolicyReader</b> method removes the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Text form of the SID to remove from the list of policy readers.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="https://msdn.microsoft.com/7dcacc91-6327-4e6c-8aa0-06e7e0191a41">PolicyReaders</a> property.



