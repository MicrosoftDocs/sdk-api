---
UID: NF:cfgmgr32.CM_Get_Next_Log_Conf
title: CM_Get_Next_Log_Conf function (cfgmgr32.h)
description: The CM_Get_Next_Log_Conf function obtains the next logical configuration associated with a specific device instance on the local machine.
helpviewer_keywords: ["CM_Get_Next_Log_Conf","CM_Get_Next_Log_Conf function [Device and Driver Installation]","cfgmgr32/CM_Get_Next_Log_Conf","cfgmgrfn_e8834764-27d4-4e23-bff0-99364b13967f.xml","devinst.cm_get_next_log_conf"]
old-location: devinst\cm_get_next_log_conf.htm
tech.root: devinst
ms.assetid: fa256bda-a7ee-4583-a91b-e7c2ef39b3f2
ms.date: 12/05/2018
ms.keywords: CM_Get_Next_Log_Conf, CM_Get_Next_Log_Conf function [Device and Driver Installation], cfgmgr32/CM_Get_Next_Log_Conf, cfgmgrfn_e8834764-27d4-4e23-bff0-99364b13967f.xml, devinst.cm_get_next_log_conf
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
 - CM_Get_Next_Log_Conf
 - cfgmgr32/CM_Get_Next_Log_Conf
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
 - CM_Get_Next_Log_Conf
---

# CM_Get_Next_Log_Conf function


## -description

The <b>CM_Get_Next_Log_Conf</b> function obtains the next <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> associated with a specific <a href="/windows-hardware/drivers/">device instance</a> on the local machine.

## -parameters

### -param plcLogConf [out, optional]

Address of a location to receive the handle to a logical configuration, or <b>NULL</b>. (See the following <b>Remarks</b> section.

### -param lcLogConf [in]

Caller-supplied handle to a logical configuration. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>


<b>CM_Get_Next_Log_Conf</b>

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Next_Log_Conf</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

To enumerate the logical configurations associated with a device instance, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a> to obtain the first logical configuration of a specified configuration type, then call <b>CM_Get_Next_Log_Conf</b> repeatedly until it returns CR_NO_MORE_LOG_CONF.

Calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a> or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf">CM_Free_Log_Conf</a> can invalidate the handle obtained from a previous call to <b>CM_Get_Next_Log_Conf</b>. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf</b> or <b>CM_Free_Log_Conf</b>, your code must call <b>CM_Get_First_Log_Conf</b> again and start at the first configuration.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>.

If <b>CM_Get_Next_Log_Conf</b> is called with <i>plcLogConf</i> set to <b>NULL</b>, no handle is returned. This allows you to use the return status to determine if a configuration exists without the need to subsequently free the handle.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a>