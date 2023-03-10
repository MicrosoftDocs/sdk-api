---
UID: NF:cfgmgr32.CM_Get_Next_Res_Des
title: CM_Get_Next_Res_Des function (cfgmgr32.h)
description: The CM_Get_Next_Res_Des function obtains a handle to the next resource descriptor, of a specified resource type, for a logical configuration on the local machine.
helpviewer_keywords: ["CM_Get_Next_Res_Des","CM_Get_Next_Res_Des function [Device and Driver Installation]","cfgmgr32/CM_Get_Next_Res_Des","cfgmgrfn_e12ec655-bb0e-4601-9e4b-7ba65a08bfac.xml","devinst.cm_get_next_res_des"]
old-location: devinst\cm_get_next_res_des.htm
tech.root: devinst
ms.assetid: 2ce2a84c-a9fe-42ff-920f-47dd0f54a820
ms.date: 12/05/2018
ms.keywords: CM_Get_Next_Res_Des, CM_Get_Next_Res_Des function [Device and Driver Installation], cfgmgr32/CM_Get_Next_Res_Des, cfgmgrfn_e12ec655-bb0e-4601-9e4b-7ba65a08bfac.xml, devinst.cm_get_next_res_des
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
 - CM_Get_Next_Res_Des
 - cfgmgr32/CM_Get_Next_Res_Des
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
 - CM_Get_Next_Res_Des
---

# CM_Get_Next_Res_Des function


## -description

The <b>CM_Get_Next_Res_Des</b> function obtains a handle to the next <a href="/windows-hardware/drivers/">resource descriptor</a>, of a specified resource type, for a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.

## -parameters

### -param prdResDes [out]

Pointer to a location to receive a resource descriptor handle.

### -param rdResDes [in]

Caller-supplied handle to either a resource descriptor or a logical configuration. For more information, see the following <b>Remarks</b> section.

### -param ForResource [in]

Caller-supplied resource type identifier, indicating the type of resource descriptor being requested. This must be one of the <b>ResType_</b>-prefixed constants defined in <i>Cfgmgr32.h</i>.

### -param pResourceID [out, optional]

Pointer to a location to receive a resource type identifier, if <i>ForResource</i> specifies <b>ResType_All</b>. For any other <i>ForResource</i> value, callers should set this to <b>NULL</b>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Next_Res_Des</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

To enumerate a logical configuration's resource descriptors, begin by calling <b>CM_Get_Next_Res_Des</b> with the logical configuration's handle as the argument for <i>rdResDes</i>. This obtains a handle to the first resource descriptor of the type specified by <i>ForResource</i>. Then for each subsequent call to <b>CM_Get_Next_Res_Des</b>, specify the most recently obtained descriptor handle as the argument for <i>rdResDes</i>. Repeat until the function returns CR_NO_MORE_RES_DES.

To retrieve the information stored in a resource descriptor, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data">CM_Get_Res_Des_Data</a>.

To modify the information stored in a resource descriptor, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des">CM_Modify_Res_Des</a>.

Callers of <b>CM_Get_Next_Res_Des</b> must call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex">CM_Get_Next_Res_Des_Ex</a>