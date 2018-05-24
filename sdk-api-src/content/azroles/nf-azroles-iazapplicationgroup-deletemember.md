---
UID: NF:azroles.IAzApplicationGroup.DeleteMember
title: IAzApplicationGroup::DeleteMember
author: windows-driver-content
description: Removes the specified security identifier (SID) in text form from the list of accounts that belong to the application group.
old-location: security\iazapplicationgroup_deletemember.htm
old-project: SecAuthZ
ms.assetid: 9db3b162-b37d-4a86-a3c0-cb594370238b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AzApplicationGroup object [Security],DeleteMember method, DeleteMember, DeleteMember method [Security], DeleteMember method [Security],AzApplicationGroup object, DeleteMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteMember method, IAzApplicationGroup.DeleteMember, IAzApplicationGroup::DeleteMember, azroles/IAzApplicationGroup::DeleteMember, security.iazapplicationgroup_deletemember
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplicationGroup.DeleteMember
-	AzApplicationGroup.DeleteMember
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::DeleteMember


## -description


The <b>DeleteMember</b> method removes  the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of  accounts that belong to the application group.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of  accounts that belong to the application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of accounts that belong to this application group in text form, use the <a href="https://msdn.microsoft.com/1370fe81-a729-477e-a500-1823abb713e1">Members</a> property.



