---
UID: NF:azroles.IAzApplicationGroup.DeleteNonMember
title: IAzApplicationGroup::DeleteNonMember
author: windows-sdk-content
description: Removes the specified security identifier (SID) in text form from the list of accounts that are refused membership in the application group.
old-location: security\iazapplicationgroup_deletenonmember.htm
tech.root: secauthz
ms.assetid: 05d58f62-fa34-4829-a535-65ea0f5144ab
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AzApplicationGroup object [Security],DeleteNonMember method, DeleteNonMember, DeleteNonMember method [Security], DeleteNonMember method [Security],AzApplicationGroup object, DeleteNonMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteNonMember method, IAzApplicationGroup.DeleteNonMember, IAzApplicationGroup::DeleteNonMember, azroles/IAzApplicationGroup::DeleteNonMember, security.iazapplicationgroup_deletenonmember
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
 - IAzApplicationGroup.DeleteNonMember
 - AzApplicationGroup.DeleteNonMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::DeleteNonMember


## -description


The <b>DeleteNonMember</b> method removes the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of  accounts that are refused membership in the application group.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of  accounts that are refused membership in the application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of accounts that are refused membership in this application group in text form, use the <a href="https://msdn.microsoft.com/43bdd205-4750-4ff6-8063-8de2c5962b09">NonMembers</a> property.



