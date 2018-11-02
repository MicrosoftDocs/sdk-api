---
UID: NF:azroles.IAzRole.AddMember
title: IAzRole::AddMember
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of Windows accounts that belong to the role.
old-location: security\iazrole_addmember.htm
tech.root: secauthz
ms.assetid: b2be62cb-7256-4031-8af9-24f3043a8430
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddMember, AddMember method [Security], AddMember method [Security],AzRole object, AddMember method [Security],IAzRole interface, AzRole object [Security],AddMember method, IAzRole interface [Security],AddMember method, IAzRole.AddMember, IAzRole::AddMember, azroles/IAzRole::AddMember, security.iazrole_addmember
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
 - IAzRole.AddMember
 - AzRole.AddMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzRole::AddMember


## -description


The <b>AddMember</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of Windows  accounts that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to add to the list of Windows  accounts that belong to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of Windows accounts that belong to this role in text form, use the <a href="https://msdn.microsoft.com/03391842-fc8a-4dc2-878e-4fe1c41cc4dd">Members</a> property.

You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



