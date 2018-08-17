---
UID: NF:azroles.IAzScope.AddPolicyReader
title: IAzScope::AddPolicyReader
author: windows-sdk-content
description: The AddPolicyReader method of IAzScope adds the specified security identifier in text form to the list of principals that act as policy readers.
old-location: security\iazscope_addpolicyreader.htm
old-project: secauthz
ms.assetid: dd4d3254-8bcf-46b5-8e7b-d3f076988a7c
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AddPolicyReader, AddPolicyReader method [Security], AddPolicyReader method [Security],AzScope object, AddPolicyReader method [Security],IAzScope interface, AzScope object [Security],AddPolicyReader method, IAzScope interface [Security],AddPolicyReader method, IAzScope.AddPolicyReader, IAzScope::AddPolicyReader, azroles/IAzScope::AddPolicyReader, security.iazscope_addpolicyreader
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
 - IAzScope.AddPolicyReader
 - AzScope.AddPolicyReader
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::AddPolicyReader


## -description


The <b>AddPolicyReader</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Text form of the SID to add to the list of policy readers.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="https://msdn.microsoft.com/7576997c-a585-4f0d-bec5-c616d39633f9">PolicyReaders</a> property.

You must call the <a href="https://msdn.microsoft.com/c06f1994-71d9-4867-a5ed-8fa90206994f">Submit</a> method to persist any changes made by this method.



