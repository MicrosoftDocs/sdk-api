---
UID: NF:cfgmgr32.CM_Add_Empty_Log_Conf
title: CM_Add_Empty_Log_Conf function (cfgmgr32.h)
description: The CM_Add_Empty_Log_Conf function creates an empty logical configuration, for a specified configuration type and a specified device instance, on the local machine.
helpviewer_keywords: ["CM_Add_Empty_Log_Conf","CM_Add_Empty_Log_Conf function [Device and Driver Installation]","cfgmgr32/CM_Add_Empty_Log_Conf","cfgmgrfn_91cca29b-dad4-43a7-882c-0cc465811429.xml","devinst.cm_add_empty_log_conf"]
old-location: devinst\cm_add_empty_log_conf.htm
tech.root: devinst
ms.assetid: 9de0b04d-96be-4c93-b7af-09200fdcf807
ms.date: 12/05/2018
ms.keywords: CM_Add_Empty_Log_Conf, CM_Add_Empty_Log_Conf function [Device and Driver Installation], cfgmgr32/CM_Add_Empty_Log_Conf, cfgmgrfn_91cca29b-dad4-43a7-882c-0cc465811429.xml, devinst.cm_add_empty_log_conf
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
 - CM_Add_Empty_Log_Conf
 - cfgmgr32/CM_Add_Empty_Log_Conf
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
 - CM_Add_Empty_Log_Conf
---

# CM_Add_Empty_Log_Conf function


## -description

The <b>CM_Add_Empty_Log_Conf</b> function creates an empty <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>, for a specified configuration type and a specified device instance, on the local machine.

## -parameters

### -param plcLogConf [out]

Address of a location to receive the handle to an empty logical configuration.

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.

### -param Priority [in]

Caller-supplied configuration priority value. This must be one of the constant values listed in the following table. The constants are listed in order of priority, from highest to lowest. (For multiple configurations with the same <i>ulFlags</i> value, the system will attempt to use the one with the highest priority first.)

<table>
<tr>
<th>Priority Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>
LCPRI_FORCECONFIG

</td>
<td>
Result of a <a href="/windows-hardware/drivers/kernel/hardware-resources">forced configuration</a>.

</td>
</tr>
<tr>
<td>
LCPRI_BOOTCONFIG

</td>
<td>
Result of a <a href="/windows-hardware/drivers/kernel/hardware-resources">boot configuration</a>.

</td>
</tr>
<tr>
<td>
LCPRI_DESIRED

</td>
<td>
Preferred configuration (better performance).

</td>
</tr>
<tr>
<td>
LCPRI_NORMAL

</td>
<td>
Workable configuration (acceptable performance).

</td>
</tr>
<tr>
<td>
LCPRI_LASTBESTCONFIG

</td>
<td>
<i>For internal use only.</i>

</td>
</tr>
<tr>
<td>
LCPRI_SUBOPTIMAL

</td>
<td>
Not a desirable configuration, but it will work.

</td>
</tr>
<tr>
<td>
LCPRI_LASTSOFTCONFIG

</td>
<td>
<i>For internal use only.</i>

</td>
</tr>
<tr>
<td>
LCPRI_RESTART

</td>
<td>
The system must be restarted

</td>
</tr>
<tr>
<td>
LCPRI_REBOOT

</td>
<td>
The system must be restarted (same as LCPRI_RESTART).

</td>
</tr>
<tr>
<td>
LCPRI_POWEROFF

</td>
<td>
The system must be shut down and powered off.

</td>
</tr>
<tr>
<td>
LCPRI_HARDRECONFIG

</td>
<td>
A jumper must be changed.

</td>
</tr>
<tr>
<td>
LCPRI_HARDWIRED

</td>
<td>
The configuration cannot be changed.

</td>
</tr>
<tr>
<td>
LCPRI_IMPOSSIBLE

</td>
<td>
The configuration cannot exist.

</td>
</tr>
<tr>
<td>
LCPRI_DISABLED

</td>
<td>
Disabled configuration.

</td>
</tr>
</table>

### -param ulFlags [in]

Caller-supplied flags that specify the type of the logical configuration. One of the following flags must be specified.

<table>
<tr>
<th>Configuration Type Flags</th>
<th>Definitions</th>
</tr>
<tr>
<td>
BASIC_LOG_CONF

</td>
<td>
Resource descriptors added to this configuration will describe a <a href="/windows-hardware/drivers/kernel/hardware-resources">basic configuration</a>.

</td>
</tr>
<tr>
<td>
FILTERED_LOG_CONF

</td>
<td>
<i>Do not use.</i> (Only the PnP manager can create a <a href="/windows-hardware/drivers/kernel/hardware-resources">filtered configuration</a>.)

</td>
</tr>
<tr>
<td>
ALLOC_LOG_CONF

</td>
<td>
<i>Do not use.</i> (Only the PnP manager can create an <a href="/windows-hardware/drivers/kernel/hardware-resources">allocated configuration</a>.)

</td>
</tr>
<tr>
<td>
BOOT_LOG_CONF

</td>
<td>
Resource descriptors added to this configuration will describe a <a href="/windows-hardware/drivers/kernel/hardware-resources">boot configuration</a>.

</td>
</tr>
<tr>
<td>
FORCED_LOG_CONF

</td>
<td>
Resource descriptors added to this configuration will describe a <a href="/windows-hardware/drivers/kernel/hardware-resources">forced configuration</a>.

</td>
</tr>
<tr>
<td>
OVERRIDE_LOG_CONF

</td>
<td>
Resource descriptors added to this configuration will describe an <a href="/windows-hardware/drivers/kernel/hardware-resources">override configuration</a>.

</td>
</tr>
</table>
 

One of the following bit flags can be ORed with the configuration type flag.

<table>
<tr>
<th>Priority Comparison Flags</th>
<th>Definitions</th>
</tr>
<tr>
<td>
PRIORITY_EQUAL_FIRST

</td>
<td>
If multiple configurations of the same type (<i>ulFlags</i>) have the same priority (<i>Priority</i>), this configuration is placed at the head of the list.

</td>
</tr>
<tr>
<td>
PRIORITY_EQUAL_LAST

</td>
<td>
(Default) If multiple configurations of the same type (<i>ulFlags</i>) have the same priority (<i>Priority</i>), this configuration is placed at the tail of the list.

</td>
</tr>
</table>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Add_Empty_Log_Conf</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>

## -remarks

Calling <b>CM_Add_Empty_Log_Conf</b> can cause the handles returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a> and <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a> to become invalid. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf</b>, your code must call <b>CM_Get_First_Log_Conf</b> again and start at the first configuration.

To remove a logical configuration created by <b>CM_Add_Empty_Log_Conf</b>, call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf">CM_Free_Log_Conf</a>.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to the local machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf">CM_Free_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle">CM_Free_Log_Conf_Handle</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child">CM_Get_Child</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a>