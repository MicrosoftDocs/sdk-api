---
UID: NF:cfgmgr32.CM_Free_Res_Des
title: CM_Free_Res_Des function (cfgmgr32.h)
description: The CM_Free_Res_Des function removes a resource descriptor from a logical configuration on the local machine.
helpviewer_keywords: ["CM_Free_Res_Des","CM_Free_Res_Des function [Device and Driver Installation]","cfgmgr32/CM_Free_Res_Des","cfgmgrfn_57d3d070-5730-4c20-a558-a52855e4d1e1.xml","devinst.cm_free_res_des"]
old-location: devinst\cm_free_res_des.htm
tech.root: devinst
ms.assetid: baef66ed-11a9-4a54-ba07-82159a9101e7
ms.date: 12/05/2018
ms.keywords: CM_Free_Res_Des, CM_Free_Res_Des function [Device and Driver Installation], cfgmgr32/CM_Free_Res_Des, cfgmgrfn_57d3d070-5730-4c20-a558-a52855e4d1e1.xml, devinst.cm_free_res_des
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
 - CM_Free_Res_Des
 - cfgmgr32/CM_Free_Res_Des
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
 - CM_Free_Res_Des
---

# CM_Free_Res_Des function


## -description

The <b>CM_Free_Res_Des</b> function removes a <a href="/windows-hardware/drivers/">resource descriptor</a> from a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.

## -parameters

### -param prdResDes [out]

Caller-supplied location to receive a handle to the configuration's previous resource descriptor. This parameter can be <b>NULL</b>. For more information, see the following <b>Remarks</b> section.

### -param rdResDes [in]

Caller-supplied handle to the resource descriptor to be removed. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex">CM_Add_Res_Des_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex">CM_Get_Next_Res_Des_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des">CM_Modify_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex">CM_Modify_Res_Des_Ex</a>

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Free_Res_Des</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Resource descriptors for each configuration are stored in an array. If you specify an address for <i>prdResDes</i>, then <b>CM_Free_Res_Des</b> returns a handle to the resource descriptor that was previous, in the array, to the one removed. If the handle specified by <i>rdResDes</i> represents the resource descriptor located first in the array, then <i>prdResDes</i> receives a handle to the logical configuration.

Note that calling <b>CM_Free_Res_Des</b> frees the resource descriptor, but not the descriptor's handle. To free the handle, call <b>CM_Free_Res_Des_Handle</b>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex">CM_Free_Res_Des_Ex</a>