---
UID: NF:dsrole.DsRoleFreeMemory
title: DsRoleFreeMemory function
author: windows-sdk-content
description: Frees memory allocated by the DsRoleGetPrimaryDomainInformation function.
old-location: ad\dsrolefreememory.htm
old-project: ad
ms.assetid: 5560dfec-2134-4e02-9c87-26d246cd5841
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: DsRoleFreeMemory, DsRoleFreeMemory function [Active Directory], _glines_dsrolefreememory, ad.dsrolefreememory, dsrole/DsRoleFreeMemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dsrole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DSROLE_SERVER_STATE, *PDSROLE_SERVER_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsRoleFreeMemory
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DsRoleFreeMemory function


## -description


The <b>DsRoleFreeMemory</b> function frees memory allocated by the <a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a> function.


## -parameters




### -param Buffer [in]

Pointer to the buffer to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service
  Functions</a>



<a href="https://msdn.microsoft.com/d54876e3-a622-4b44-a597-db0f710f7758">DsRoleGetPrimaryDomainInformation</a>
 

 

