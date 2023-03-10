---
UID: NF:cfgmgr32.CM_Modify_Res_Des
title: CM_Modify_Res_Des function (cfgmgr32.h)
description: The CM_Modify_Res_Des function modifies a specified resource descriptor on the local machine.
helpviewer_keywords: ["CM_Modify_Res_Des","CM_Modify_Res_Des function [Device and Driver Installation]","cfgmgr32/CM_Modify_Res_Des","cfgmgrfn_7bf5dade-d4e6-4460-8b3c-a4b99458ed28.xml","devinst.cm_modify_res_des"]
old-location: devinst\cm_modify_res_des.htm
tech.root: devinst
ms.assetid: 9320c396-4da8-4b35-a620-4bb7cbd80e9a
ms.date: 12/05/2018
ms.keywords: CM_Modify_Res_Des, CM_Modify_Res_Des function [Device and Driver Installation], cfgmgr32/CM_Modify_Res_Des, cfgmgrfn_7bf5dade-d4e6-4460-8b3c-a4b99458ed28.xml, devinst.cm_modify_res_des
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
 - CM_Modify_Res_Des
 - cfgmgr32/CM_Modify_Res_Des
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
 - CM_Modify_Res_Des
---

# CM_Modify_Res_Des function


## -description

The <b>CM_Modify_Res_Des</b> function modifies a specified resource descriptor on the local machine.

## -parameters

### -param prdResDes [out]

Pointer to a location to receive a handle to the modified resource descriptor.

### -param rdResDes [in]

Caller-supplied handle to the resource descriptor to be modified. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex">CM_Add_Res_Des_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex">CM_Get_Next_Res_Des_Ex</a>


<b>CM_Modify_Res_Des</b>


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex">CM_Modify_Res_Des_Ex</a>

### -param ResourceID [in]

Caller-supplied resource type identifier. This must be one of the <b>ResType_</b>-prefixed constants defined in <i>Cfgmgr32.h</i>.

### -param ResourceData [in]

Caller-supplied pointer to a resource descriptor, which can be one of the structures listed under the <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a> function's description of <i>ResourceData</i>.

### -param ResourceLen [in]

Caller-supplied length of the structure pointed to by <i>ResourceData</i>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Modify_Res_Des</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

The caller-supplied resource descriptor data replaces the existing data. The values specified for <i>ResourceID</i> and <i>ResourceLen</i> do not have to match the existing resource descriptor.

If the value specified for <i>ResourceID</i> is <b>ResType_ClassSpecific</b>, then the specified resource descriptor must be the last one associated with the logical configuration.

Callers of <b>CM_Modify_Res_Des</b> must call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex">CM_Modify_Res_Des_Ex</a>