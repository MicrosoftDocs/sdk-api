---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyReader
title: IAzAuthorizationStore::AddPolicyReader
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy readers.
old-location: security\azauthorizationstore_addpolicyreader.htm
old-project: secauthz
ms.assetid: 52872839-1066-4a43-8549-b7f37a0ebe40
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AddPolicyReader, AddPolicyReader method [Security], AddPolicyReader method [Security],AzAuthorizationStore object, AddPolicyReader method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyReader method, IAzAuthorizationStore interface [Security],AddPolicyReader method, IAzAuthorizationStore.AddPolicyReader, IAzAuthorizationStore::AddPolicyReader, azroles/IAzAuthorizationStore::AddPolicyReader, security.azauthorizationstore_addpolicyreader
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
 - AzAuthorizationStore.AddPolicyReader
 - IAzAuthorizationStore.AddPolicyReader
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::AddPolicyReader


## -description


The <b>AddPolicyReader</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Text form of the  SID to add to the list of policy readers.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="https://msdn.microsoft.com/22479ced-b393-40d3-bb16-f3c3e595dacf">PolicyReaders</a> property.

You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



