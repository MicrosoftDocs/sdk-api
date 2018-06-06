---
UID: NF:azroles.IAzApplication.AddPolicyReader
title: IAzApplication::AddPolicyReader
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy readers.
old-location: security\iazapplication_addpolicyreader.htm
old-project: SecAuthZ
ms.assetid: fb44461c-e494-4393-bdcd-0e759f6fbae1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddPolicyReader, AddPolicyReader method [Security], AddPolicyReader method [Security],AzApplication object, AddPolicyReader method [Security],IAzApplication interface, AzApplication object [Security],AddPolicyReader method, IAzApplication interface [Security],AddPolicyReader method, IAzApplication.AddPolicyReader, IAzApplication::AddPolicyReader, azroles/IAzApplication::AddPolicyReader, security.iazapplication_addpolicyreader
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.AddPolicyReader
 - AzApplication.AddPolicyReader
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::AddPolicyReader


## -description


The <b>AddPolicyReader</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Text form of the SID to add to the list of policy readers.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="https://msdn.microsoft.com/7dcacc91-6327-4e6c-8aa0-06e7e0191a41">PolicyReaders</a> property.

You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



