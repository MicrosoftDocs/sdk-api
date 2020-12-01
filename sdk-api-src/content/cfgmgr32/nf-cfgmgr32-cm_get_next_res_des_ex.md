---
UID: NF:cfgmgr32.CM_Get_Next_Res_Des_Ex
title: CM_Get_Next_Res_Des_Ex function (cfgmgr32.h)
description: The CM_Get_Next_Res_Des_Ex function obtains a handle to the next resource descriptor, of a specified resource type, for a logical configuration on a local or a remote machine.
helpviewer_keywords: ["CM_Get_Next_Res_Des_Ex","CM_Get_Next_Res_Des_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Next_Res_Des_Ex","cfgmgrfn_2c25fbc8-7434-4a94-817e-2c7cd8d9fa99.xml","devinst.cm_get_next_res_des_ex"]
old-location: devinst\cm_get_next_res_des_ex.htm
tech.root: devinst
ms.assetid: 91e9a686-2465-4ae8-9cc2-391cd98c2138
ms.date: 12/05/2018
ms.keywords: CM_Get_Next_Res_Des_Ex, CM_Get_Next_Res_Des_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Next_Res_Des_Ex, cfgmgrfn_2c25fbc8-7434-4a94-817e-2c7cd8d9fa99.xml, devinst.cm_get_next_res_des_ex
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
 - CM_Get_Next_Res_Des_Ex
 - cfgmgr32/CM_Get_Next_Res_Des_Ex
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
 - CM_Get_Next_Res_Des_Ex
---

# CM_Get_Next_Res_Des_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a> instead.]

The <b>CM_Get_Next_Res_Des_Ex</b> function obtains a handle to the next <a href="/windows-hardware/drivers/">resource descriptor</a>, of a specified resource type, for a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on a local or a remote machine.

## -parameters

### -param prdResDes [out]

Pointer to a location to receive a resource descriptor handle.

### -param rdResDes [in]

Caller-supplied handle to either a resource descriptor or a logical configuration. For more information, see the following <b>Remarks</b> section.

### -param ForResource [in]

Caller-supplied resource type identifier, indicating the type of resource descriptor being requested. This must be one of the ResType_-prefixed constants defined in <i>Cfgmgr32.h</i>.

### -param pResourceID [out, optional]

Pointer to a location to receive a resource type identifier, if <i>ForResource</i> specifies <b>ResType_All</b>. For any other <i>ForResource</i> value, callers should set this to <b>NULL</b>.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Next_Res_Des_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

To enumerate a logical configuration's resource descriptors, begin by calling <b>CM_Get_Next_Res_Des_Ex</b> with the logical configuration's handle as the argument for <i>rdResDes</i>. This obtains a handle to the first resource descriptor of the type specified by <i>ForResource</i>. Then for each subsequent call to <b>CM_Get_Next_Res_Des_Ex</b>, specify the most recently obtained descriptor handle as the argument for <i>rdResDes</i>. Repeat until the function returns CR_NO_MORE_RES_DES.

To retrieve the information stored in a resource descriptor, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex">CM_Get_Res_Des_Data_Ex</a>.

To modify the information stored in a resource descriptor, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex">CM_Modify_Res_Des_Ex</a>.

Callers of <b>CM_Get_Next_Res_Des_Ex</b> must call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>