---
UID: NF:cfgmgr32.CM_Add_Empty_Log_Conf_Ex
title: CM_Add_Empty_Log_Conf_Ex function (cfgmgr32.h)
description: The CM_Add_Empty_Log_Conf_Ex function creates an empty logical configuration, for a specified configuration type and a specified device instance, on either the local or a remote machine.
helpviewer_keywords: ["CM_Add_Empty_Log_Conf_Ex","CM_Add_Empty_Log_Conf_Ex function [Device and Driver Installation]","cfgmgr32/CM_Add_Empty_Log_Conf_Ex","cfgmgrfn_5cbb39e6-bde8-4677-b099-25e30e618569.xml","devinst.cm_add_empty_log_conf_ex"]
old-location: devinst\cm_add_empty_log_conf_ex.htm
tech.root: devinst
ms.assetid: cb34e5ec-4257-4c30-890a-40f669f1dfeb
ms.date: 12/05/2018
ms.keywords: CM_Add_Empty_Log_Conf_Ex, CM_Add_Empty_Log_Conf_Ex function [Device and Driver Installation], cfgmgr32/CM_Add_Empty_Log_Conf_Ex, cfgmgrfn_5cbb39e6-bde8-4677-b099-25e30e618569.xml, devinst.cm_add_empty_log_conf_ex
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
 - CM_Add_Empty_Log_Conf_Ex
 - cfgmgr32/CM_Add_Empty_Log_Conf_Ex
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
 - CM_Add_Empty_Log_Conf_Ex
---

# CM_Add_Empty_Log_Conf_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a> instead.]

The <b>CM_Add_Empty_Log_Conf_Ex</b> function creates an empty <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>, for a specified configuration type and a specified device instance, on either the local or a remote machine.

## -parameters

### -param plcLogConf [out]

Pointer to a location to receive the handle to an empty logical configuration.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param Priority [in]

Caller-supplied configuration priority value. For a list of values, see the <i>Priority</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>.

### -param ulFlags [in]

Caller-supplied flags that specify the type of the logical configuration. For a list of flags, see the description <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Add_Empty_Log_Conf_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Calling <b>CM_Add_Empty_Log_Conf_Ex</b> can cause the handles returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex">CM_Get_First_Log_Conf_Ex</a> and <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a> to become invalid. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf_Ex</b>, your code must call <b>CM_Get_First_Log_Conf_Ex</b> again and start at the first configuration.

To remove a logical configuration created by <b>CM_Add_Empty_Log_Conf_Ex</b>, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex">CM_Free_Log_Conf_Ex</a>.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex">CM_Free_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex">CM_Get_First_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a>