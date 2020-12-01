---
UID: NF:dsrole.DsRoleFreeMemory
title: DsRoleFreeMemory function (dsrole.h)
description: Frees memory allocated by the DsRoleGetPrimaryDomainInformation function.
helpviewer_keywords: ["DsRoleFreeMemory","DsRoleFreeMemory function [Active Directory]","_glines_dsrolefreememory","ad.dsrolefreememory","dsrole/DsRoleFreeMemory"]
old-location: ad\dsrolefreememory.htm
tech.root: ad
ms.assetid: 5560dfec-2134-4e02-9c87-26d246cd5841
ms.date: 12/05/2018
ms.keywords: DsRoleFreeMemory, DsRoleFreeMemory function [Active Directory], _glines_dsrolefreememory, ad.dsrolefreememory, dsrole/DsRoleFreeMemory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsRoleFreeMemory
 - dsrole/DsRoleFreeMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsRoleFreeMemory
---

# DsRoleFreeMemory function


## -description

The <b>DsRoleFreeMemory</b> function frees memory allocated by the <a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a> function.

## -parameters

### -param Buffer [in]

Pointer to the buffer to be freed.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service
  Functions</a>



<a href="/windows/desktop/api/dsrole/nf-dsrole-dsrolegetprimarydomaininformation">DsRoleGetPrimaryDomainInformation</a>