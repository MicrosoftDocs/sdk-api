---
UID: NF:cfgmgr32.CM_Get_Res_Des_Data
title: CM_Get_Res_Des_Data function (cfgmgr32.h)
description: The CM_Get_Res_Des_Data function retrieves the information stored in a resource descriptor on the local machine.
helpviewer_keywords: ["CM_Get_Res_Des_Data","CM_Get_Res_Des_Data function [Device and Driver Installation]","cfgmgr32/CM_Get_Res_Des_Data","cfgmgrfn_76c92157-2495-4c52-a25f-9a02d83cff75.xml","devinst.cm_get_res_des_data"]
old-location: devinst\cm_get_res_des_data.htm
tech.root: devinst
ms.assetid: f35975ac-022e-4e7c-a331-da0ccd0440a1
ms.date: 12/05/2018
ms.keywords: CM_Get_Res_Des_Data, CM_Get_Res_Des_Data function [Device and Driver Installation], cfgmgr32/CM_Get_Res_Des_Data, cfgmgrfn_76c92157-2495-4c52-a25f-9a02d83cff75.xml, devinst.cm_get_res_des_data
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
 - CM_Get_Res_Des_Data
 - cfgmgr32/CM_Get_Res_Des_Data
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
 - CM_Get_Res_Des_Data
---

# CM_Get_Res_Des_Data function


## -description

The <b>CM_Get_Res_Des_Data</b> function retrieves the information stored in a <a href="/windows-hardware/drivers/">resource descriptor</a> on the local machine.

## -parameters

### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a>.

### -param Buffer [out]

Address of a buffer to receive the contents of a resource descriptor. The required buffer size should be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size">CM_Get_Res_Des_Data_Size</a>.

### -param BufferLen [in]

Caller-supplied length of the buffer specified by <i>Buffer</i>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Information returned in the buffer supplied by <i>Buffer</i> will be formatted as one of the resource type structures listed in the description of <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>, based on the resource type that was specified when <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_res_des">CM_Get_Next_Res_Des</a> was called to obtain the resource descriptor handle.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex">CM_Get_Res_Des_Data_Ex</a>