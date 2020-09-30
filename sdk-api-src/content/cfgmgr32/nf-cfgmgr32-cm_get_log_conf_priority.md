---
UID: NF:cfgmgr32.CM_Get_Log_Conf_Priority
title: CM_Get_Log_Conf_Priority function (cfgmgr32.h)
description: The CM_Get_Log_Conf_Priority function obtains the configuration priority of a specified logical configuration on the local machine.
helpviewer_keywords: ["CM_Get_Log_Conf_Priority","CM_Get_Log_Conf_Priority function [Device and Driver Installation]","cfgmgr32/CM_Get_Log_Conf_Priority","cfgmgrfn_23c7a94b-fd43-493e-ae6b-56ce7c69278b.xml","devinst.cm_get_log_conf_priority"]
old-location: devinst\cm_get_log_conf_priority.htm
tech.root: devinst
ms.assetid: 0db6c2f4-2d44-49ad-a1cc-f29a5088c74c
ms.date: 12/05/2018
ms.keywords: CM_Get_Log_Conf_Priority, CM_Get_Log_Conf_Priority function [Device and Driver Installation], cfgmgr32/CM_Get_Log_Conf_Priority, cfgmgrfn_23c7a94b-fd43-493e-ae6b-56ce7c69278b.xml, devinst.cm_get_log_conf_priority
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
 - CM_Get_Log_Conf_Priority
 - cfgmgr32/CM_Get_Log_Conf_Priority
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
 - CM_Get_Log_Conf_Priority
---

# CM_Get_Log_Conf_Priority function


## -description

The <b>CM_Get_Log_Conf_Priority</b> function obtains the configuration priority of a specified <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.

## -parameters

### -param lcLogConf [in]

Caller-supplied handle to a logical configuration. This handle must have been previously obtained by calling one of the following functions:


<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex">CM_Get_First_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a>

### -param pPriority [out]

Caller-supplied address of a location to receive a configuration priority value. For a list of priority values, see the description of <i>Priority</i> for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>.

### -param ulFlags [in]

Not used, must be zero.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Log_Conf_Priority</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex">CM_Get_Log_Conf_Priority_Ex</a>