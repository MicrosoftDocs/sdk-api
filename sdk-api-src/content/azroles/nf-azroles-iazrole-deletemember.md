---
UID: NF:azroles.IAzRole.DeleteMember
title: IAzRole::DeleteMember
author: windows-sdk-content
description: Removes the specified security identifier (SID) in text form from the list of Windows accounts that belong to the role.
old-location: security\iazrole_deletemember.htm
tech.root: SecAuthZ
ms.assetid: 676f0469-f57f-4f3f-8295-b9c99eb13de8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzRole object [Security],DeleteMember method, DeleteMember, DeleteMember method [Security], DeleteMember method [Security],AzRole object, DeleteMember method [Security],IAzRole interface, IAzRole interface [Security],DeleteMember method, IAzRole.DeleteMember, IAzRole::DeleteMember, azroles/IAzRole::DeleteMember, security.iazrole_deletemember
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
 - IAzRole.DeleteMember
 - AzRole.DeleteMember
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzRole::DeleteMember


## -description


The <b>DeleteMember</b> method removes  the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of Windows  accounts that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of Windows  accounts that belong to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of Windows accounts that belong to the role in text form, use the <a href="https://msdn.microsoft.com/03391842-fc8a-4dc2-878e-4fe1c41cc4dd">Members</a> property.



