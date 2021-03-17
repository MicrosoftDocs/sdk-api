---
UID: NF:cfgmgr32.CM_Free_Res_Des_Handle
title: CM_Free_Res_Des_Handle function (cfgmgr32.h)
description: The CM_Free_Res_Des_Handle function invalidates a resource description handle and frees its associated memory allocation.
helpviewer_keywords: ["CM_Free_Res_Des_Handle","CM_Free_Res_Des_Handle function [Device and Driver Installation]","cfgmgr32/CM_Free_Res_Des_Handle","cfgmgrfn_a3dd0de4-8188-4117-9e8b-ecc5eb448096.xml","devinst.cm_free_res_des_handle"]
old-location: devinst\cm_free_res_des_handle.htm
tech.root: devinst
ms.assetid: 4a585d64-fd00-47a8-8ada-7e343beb829d
ms.date: 12/05/2018
ms.keywords: CM_Free_Res_Des_Handle, CM_Free_Res_Des_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Res_Des_Handle, cfgmgrfn_a3dd0de4-8188-4117-9e8b-ecc5eb448096.xml, devinst.cm_free_res_des_handle
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Free_Res_Des_Handle
 - cfgmgr32/CM_Free_Res_Des_Handle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Free_Res_Des_Handle
---

# CM_Free_Res_Des_Handle function


## -description

The <b>CM_Free_Res_Des_Handle</b> function invalidates a resource description handle and frees its associated memory allocation.

## -parameters

### -param rdResDes [in]

Caller-supplied resource descriptor handle to be freed. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex">CM_Add_Res_Des_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex">CM_Get_Next_Res_Des_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des">CM_Modify_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex">CM_Modify_Res_Des_Ex</a>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Each time your code calls one of the functions listed under the description of <i>rdResDes</i>, it must subsequently call <b>CM_Free_Res_Des_Handle</b>.