---
UID: NF:cfgmgr32.CM_Get_Log_Conf_Priority_Ex
title: CM_Get_Log_Conf_Priority_Ex function (cfgmgr32.h)
description: The CM_Get_Log_Conf_Priority_Ex function obtains the configuration priority of a specified logical configuration on a local or a remote machine.
helpviewer_keywords: ["CM_Get_Log_Conf_Priority_Ex","CM_Get_Log_Conf_Priority_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Log_Conf_Priority_Ex","cfgmgrfn_f4e7d475-18c7-4854-bff1-a484014f07ac.xml","devinst.cm_get_log_conf_priority_ex"]
old-location: devinst\cm_get_log_conf_priority_ex.htm
tech.root: devinst
ms.assetid: e02e8885-b459-4a70-9f0d-7765603e9dc4
ms.date: 12/05/2018
ms.keywords: CM_Get_Log_Conf_Priority_Ex, CM_Get_Log_Conf_Priority_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Log_Conf_Priority_Ex, cfgmgrfn_f4e7d475-18c7-4854-bff1-a484014f07ac.xml, devinst.cm_get_log_conf_priority_ex
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
 - CM_Get_Log_Conf_Priority_Ex
 - cfgmgr32/CM_Get_Log_Conf_Priority_Ex
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
 - CM_Get_Log_Conf_Priority_Ex
---

# CM_Get_Log_Conf_Priority_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority">CM_Get_Log_Conf_Priority</a> instead.]

The <b>CM_Get_Log_Conf_Priority_Ex</b> function obtains the configuration priority of a specified <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on a local or a remote machine.

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

Caller-supplied address of a location to receive a configuration priority value. For a list of priority values, see the description of <i>Priority</i> for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>.

### -param ulFlags [in]

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Log_Conf_Priority_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority">CM_Get_Log_Conf_Priority</a>