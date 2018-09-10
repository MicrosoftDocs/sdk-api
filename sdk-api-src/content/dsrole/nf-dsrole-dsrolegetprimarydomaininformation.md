---
UID: NF:dsrole.DsRoleGetPrimaryDomainInformation
title: DsRoleGetPrimaryDomainInformation function
author: windows-sdk-content
description: Retrieves state data for the computer.
old-location: ad\dsrolegetprimarydomaininformation.htm
tech.root: ad
ms.assetid: d54876e3-a622-4b44-a597-db0f710f7758
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DsRoleGetPrimaryDomainInformation, DsRoleGetPrimaryDomainInformation function [Active Directory], _glines_dsrolegetprimarydomaininformation, ad.dsrolegetprimarydomaininformation, dsrole/DsRoleGetPrimaryDomainInformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsRoleGetPrimaryDomainInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsRoleGetPrimaryDomainInformation function


## -description


The <b>DsRoleGetPrimaryDomainInformation</b> function retrieves state data for the computer. This data includes the state of the directory service installation and domain data.


## -parameters




### -param lpServer [in]

Pointer to null-terminated Unicode string that contains the name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.


### -param InfoLevel [in]

Contains one of the <a href="https://msdn.microsoft.com/c8b141b1-d5fa-4ec9-8899-a1b0f6a4ce1d">DSROLE_PRIMARY_DOMAIN_INFO_LEVEL</a> values that specify the type of data to retrieve. This parameter also determines the format of the data supplied in <i>Buffer</i>.


### -param Buffer [out]

Pointer to the address of a buffer that receives the requested data. The format of this data depends on the value of the <i>InfoLevel</i> parameter.

The caller must free this memory when it is no longer required by calling <a href="https://msdn.microsoft.com/5560dfec-2134-4e02-9c87-26d246cd5841">DsRoleFreeMemory</a>.


## -returns



If the function is successful, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/c6c8e510-190a-47ad-805c-b8d3fbee836d">DSROLE_OPERATION_STATE_INFO</a>



<a href="https://msdn.microsoft.com/8a7b34e8-46d6-46dc-9fef-ec37b0f65eea">DSROLE_PRIMARY_DOMAIN_INFO_BASIC</a>



<a href="https://msdn.microsoft.com/c368d8d9-a91d-4013-880e-36a47d42a697">DSROLE_UPGRADE_STATUS_INFO</a>



<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/5560dfec-2134-4e02-9c87-26d246cd5841">DsRoleFreeMemory</a>
 

 

