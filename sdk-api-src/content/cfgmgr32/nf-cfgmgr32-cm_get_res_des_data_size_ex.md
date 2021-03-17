---
UID: NF:cfgmgr32.CM_Get_Res_Des_Data_Size_Ex
title: CM_Get_Res_Des_Data_Size_Ex function (cfgmgr32.h)
description: The CM_Get_Res_Des_Data_Size_Ex function obtains the buffer size required to hold the information contained in a specified resource descriptor on a local or a remote machine.
helpviewer_keywords: ["CM_Get_Res_Des_Data_Size_Ex","CM_Get_Res_Des_Data_Size_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Res_Des_Data_Size_Ex","cfgmgrfn_5ea04040-e1eb-4e2c-94bf-906e0ea45791.xml","devinst.cm_get_res_des_data_size_ex"]
old-location: devinst\cm_get_res_des_data_size_ex.htm
tech.root: devinst
ms.assetid: 59b96655-aea9-4f98-9f6a-1a9093db9c63
ms.date: 12/05/2018
ms.keywords: CM_Get_Res_Des_Data_Size_Ex, CM_Get_Res_Des_Data_Size_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Res_Des_Data_Size_Ex, cfgmgrfn_5ea04040-e1eb-4e2c-94bf-906e0ea45791.xml, devinst.cm_get_res_des_data_size_ex
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
 - CM_Get_Res_Des_Data_Size_Ex
 - cfgmgr32/CM_Get_Res_Des_Data_Size_Ex
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
 - CM_Get_Res_Des_Data_Size_Ex
---

# CM_Get_Res_Des_Data_Size_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size">CM_Get_Res_Des_Data_Size</a> instead.]

The <b>CM_Get_Res_Des_Data_Size_Ex</b> function obtains the buffer size required to hold the information contained in a specified <a href="/windows-hardware/drivers/">resource descriptor</a> on a local or a remote machine.

## -parameters

### -param pulSize [out]

Caller-supplied address of a location to receive the required buffer size.

### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex">CM_Get_Next_Res_Des_Ex</a>.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data_Size_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

The returned size value represents the size of the appropriate resource structure (see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex">CM_Add_Res_Des_Ex</a>). If the resource descriptor resides in a resource requirements list, the returned size includes both the size of the resource structure and the space allocated for associated range arrays.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size">CM_Get_Res_Des_Data_Size</a>