---
UID: NF:cfgmgr32.CM_Get_Res_Des_Data_Size
title: CM_Get_Res_Des_Data_Size function (cfgmgr32.h)
description: The CM_Get_Res_Des_Data_Size function obtains the buffer size required to hold the information contained in a specified resource descriptor on the local machine.
helpviewer_keywords: ["CM_Get_Res_Des_Data_Size","CM_Get_Res_Des_Data_Size function [Device and Driver Installation]","cfgmgr32/CM_Get_Res_Des_Data_Size","cfgmgrfn_bc279907-eb02-45fc-801d-48dde3d046a9.xml","devinst.cm_get_res_des_data_size"]
old-location: devinst\cm_get_res_des_data_size.htm
tech.root: devinst
ms.assetid: 51337d09-2ebb-45fd-82cd-2362093fb7ff
ms.date: 12/05/2018
ms.keywords: CM_Get_Res_Des_Data_Size, CM_Get_Res_Des_Data_Size function [Device and Driver Installation], cfgmgr32/CM_Get_Res_Des_Data_Size, cfgmgrfn_bc279907-eb02-45fc-801d-48dde3d046a9.xml, devinst.cm_get_res_des_data_size
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
 - CM_Get_Res_Des_Data_Size
 - cfgmgr32/CM_Get_Res_Des_Data_Size
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
 - CM_Get_Res_Des_Data_Size
---

# CM_Get_Res_Des_Data_Size function


## -description

The <b>CM_Get_Res_Des_Data_Size</b> function obtains the buffer size required to hold the information contained in a specified <a href="/windows-hardware/drivers/">resource descriptor</a> on the local machine.

## -parameters

### -param pulSize [out]

Caller-supplied address of a location to receive the required buffer size.

### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data_Size</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

The returned size value represents the size of the appropriate resource structure (see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>). If the resource descriptor resides in a resource requirements list, the returned size includes both the size of the resource structure and the space allocated for associated range arrays.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex">CM_Get_Res_Des_Data_Size_Ex</a>