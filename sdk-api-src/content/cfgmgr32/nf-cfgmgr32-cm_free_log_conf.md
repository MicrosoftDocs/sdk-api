---
UID: NF:cfgmgr32.CM_Free_Log_Conf
title: CM_Free_Log_Conf function (cfgmgr32.h)
description: The CM_Free_Log_Conf function removes a logical configuration and all associated resource descriptors from the local machine.
helpviewer_keywords: ["CM_Free_Log_Conf","CM_Free_Log_Conf function [Device and Driver Installation]","cfgmgr32/CM_Free_Log_Conf","cfgmgrfn_68a9c019-f83c-4453-a988-3e9b1b33dd5f.xml","devinst.cm_free_log_conf"]
old-location: devinst\cm_free_log_conf.htm
tech.root: devinst
ms.assetid: 89d8e5ed-751c-4f85-8669-a33c6228fe22
ms.date: 12/05/2018
ms.keywords: CM_Free_Log_Conf, CM_Free_Log_Conf function [Device and Driver Installation], cfgmgr32/CM_Free_Log_Conf, cfgmgrfn_68a9c019-f83c-4453-a988-3e9b1b33dd5f.xml, devinst.cm_free_log_conf
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
 - CM_Free_Log_Conf
 - cfgmgr32/CM_Free_Log_Conf
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
 - CM_Free_Log_Conf
---

# CM_Free_Log_Conf function


## -description

The <b>CM_Free_Log_Conf</b> function removes a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> and all associated <a href="/windows-hardware/drivers/">resource descriptors</a> from the local machine.

## -parameters

### -param lcLogConfToBeFreed [in]

Caller-supplied handle to a logical configuration. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex">CM_Get_First_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a>

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Free_Log_Conf</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Calling <b>CM_Free_Log_Conf</b> can cause the handles returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a> and <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a> to become invalid. Thus if you want to obtain logical configurations after calling <b>CM_Free_Log_Conf</b>, your code must call <b>CM_Get_First_Log_Conf</b> again and start at the first configuration.

Note that calling <b>CM_Free_Log_Conf</b> frees the configuration, but not the configuration's handle. To free the handle, call <b>CM_Free_Log_Conf_Handle</b>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex">CM_Free_Log_Conf_Ex</a>