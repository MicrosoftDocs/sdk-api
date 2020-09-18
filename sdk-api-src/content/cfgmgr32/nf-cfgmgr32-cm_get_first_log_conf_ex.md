---
UID: NF:cfgmgr32.CM_Get_First_Log_Conf_Ex
title: CM_Get_First_Log_Conf_Ex function (cfgmgr32.h)
description: The CM_Get_First_Log_Conf_Ex function obtains the first logical configuration associated with a specified device instance on a local or a remote machine.
helpviewer_keywords: ["CM_Get_First_Log_Conf_Ex","CM_Get_First_Log_Conf_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_First_Log_Conf_Ex","cfgmgrfn_bfb585c9-0dba-4c24-991e-2e866e3e6e9b.xml","devinst.cm_get_first_log_conf_ex"]
old-location: devinst\cm_get_first_log_conf_ex.htm
tech.root: devinst
ms.assetid: cb562b5c-eb40-4be4-89a3-0e69a78ae6ea
ms.date: 12/05/2018
ms.keywords: CM_Get_First_Log_Conf_Ex, CM_Get_First_Log_Conf_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_First_Log_Conf_Ex, cfgmgrfn_bfb585c9-0dba-4c24-991e-2e866e3e6e9b.xml, devinst.cm_get_first_log_conf_ex
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
 - CM_Get_First_Log_Conf_Ex
 - cfgmgr32/CM_Get_First_Log_Conf_Ex
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
 - CM_Get_First_Log_Conf_Ex
---

# CM_Get_First_Log_Conf_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a> instead.]

The <b>CM_Get_First_Log_Conf_Ex</b> function obtains the first <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> associated with a specified <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.

## -parameters

### -param plcLogConf [out, optional]

Address of a location to receive the handle to a logical configuration, or <b>NULL</b>. See the <b>Remarks</b> section.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param ulFlags [in]

Caller-supplied flag value indicating the type of logical configuration being requested. For a list of flags, see the <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_First_Log_Conf_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a> or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex">CM_Free_Log_Conf_Ex</a> can invalidate the handle obtained from a previous call to <b>CM_Get_First_Log_Conf_Ex</b>. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf_Ex</b> or <b>CM_Free_Log_Conf_Ex</b>, your code must call <b>CM_Get_First_Log_Conf_Ex</b> again and start at the first configuration.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>.

If <b>CM_Get_First_Log_Conf_Ex</b> is called with <i>plcLogConf</i> set to <b>NULL</b>, no handle is returned. This allows you to use the return status to determine if a configuration exists without the need to subsequently free the handle.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex">CM_Free_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>



<b>CM_Get_First_Log_Conf</b>