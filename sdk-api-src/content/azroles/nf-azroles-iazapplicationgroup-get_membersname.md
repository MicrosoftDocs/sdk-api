---
UID: NF:azroles.IAzApplicationGroup.get_MembersName
title: IAzApplicationGroup::get_MembersName
author: windows-sdk-content
description: Retrieves the account names of accounts that belong to the application group.
old-location: security\iazapplicationgroup_membersname.htm
old-project: SecAuthZ
ms.assetid: bdd6f88f-ea06-4075-b563-d0c7707107f8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzApplicationGroup object [Security],MembersName property, IAzApplicationGroup interface [Security],MembersName property, IAzApplicationGroup.MembersName, IAzApplicationGroup.get_MembersName, IAzApplicationGroup::MembersName, IAzApplicationGroup::get_MembersName, MembersName property [Security], MembersName property [Security],AzApplicationGroup object, MembersName property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::MembersName, azroles/IAzApplicationGroup::get_MembersName, get_MembersName, security.iazapplicationgroup_membersname
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
 - IAzApplicationGroup.MembersName
 - IAzApplicationGroup.get_MembersName
 - AzApplicationGroup.MembersName
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::get_MembersName


## -description


The <b>MembersName</b> property retrieves the account names of  accounts that belong to the application group.

This property is read-only.


## -parameters


## -remarks



This property is ignored unless the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="https://msdn.microsoft.com/library/ms221482(v=VS.85).aspx">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



