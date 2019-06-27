---
UID: NF:azroles.IAzApplicationGroup.AddMember
title: IAzApplicationGroup::AddMember (azroles.h)
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of accounts that belong to the application group.
old-location: security\iazapplicationgroup_addmember.htm
tech.root: SecAuthZ
ms.assetid: 934ca397-2067-451a-bccd-103ab4db3b1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddMember, AddMember method [Security], AddMember method [Security],AzApplicationGroup object, AddMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddMember method, IAzApplicationGroup interface [Security],AddMember method, IAzApplicationGroup.AddMember, IAzApplicationGroup::AddMember, azroles/IAzApplicationGroup::AddMember, security.iazapplicationgroup_addmember
ms.topic: method
f1_keywords: 
 - "azroles/IAzApplicationGroup.AddMember"
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
 - IAzApplicationGroup.AddMember
 - AzApplicationGroup.AddMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::AddMember


## -description


The <b>AddMember</b> method adds the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of  accounts that belong to the application group.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to add to the list of  accounts that belong to the application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of accounts that belong to this application group in text form, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a> property.

You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.



