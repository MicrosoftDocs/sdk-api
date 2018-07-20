---
UID: NF:cfgmgr32.CM_Get_First_Log_Conf
title: CM_Get_First_Log_Conf function
author: windows-sdk-content
description: The CM_Get_First_Log_Conf function obtains the first logical configuration, of a specified configuration type, associated with a specified device instance on the local machine.
old-location: devinst\cm_get_first_log_conf.htm
old-project: devinst
ms.assetid: 7ef14797-ea67-40cb-ad8d-e8c846ae1fd4
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: CM_Get_First_Log_Conf, CM_Get_First_Log_Conf function [Device and Driver Installation], cfgmgr32/CM_Get_First_Log_Conf, cfgmgrfn_5310503c-65cc-4185-9d26-bf29c1af74c4.xml, devinst.cm_get_first_log_conf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_First_Log_Conf
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_First_Log_Conf function


## -description


The <b>CM_Get_First_Log_Conf</b> function obtains the first <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a>, of a specified configuration type, associated with a specified <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on the local machine.


## -parameters




### -param plcLogConf [out, optional]

Address of a location to receive the handle to a logical configuration, or <b>NULL</b>. See the following <b>Remarks</b> section.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Caller-supplied flag value indicating the type of logical configuration being requested. One of the flags in the following table must be specified.

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
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">basic configuration</a> information.

</td>
</tr>
<tr>
<td>
FILTERED_LOG_CONF

</td>
<td>
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">filtered configuration</a> information.

</td>
</tr>
<tr>
<td>
ALLOC_LOG_CONF

</td>
<td>
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">allocated configuration</a> information.

</td>
</tr>
<tr>
<td>
BOOT_LOG_CONF

</td>
<td>
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">boot configuration</a> information.

</td>
</tr>
<tr>
<td>
FORCED_LOG_CONF

</td>
<td>
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">forced configuration</a> information.

</td>
</tr>
<tr>
<td>
OVERRIDE_LOG_CONF

</td>
<td>
The caller is requesting <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">override configuration</a> information.

</td>
</tr>
</table>
 


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_First_Log_Conf</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff537921">CM_Add_Empty_Log_Conf</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538041">CM_Free_Log_Conf</a> can invalidate the handle obtained from a previous call to <b>CM_Get_First_Log_Conf</b>. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf</b> or <b>CM_Free_Log_Conf</b>, your code must call <b>CM_Get_First_Log_Conf</b> again and start at the first configuration.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538046">CM_Free_Log_Conf_Handle</a>.

If <b>CM_Get_First_Log_Conf</b> is called with <i>plcLogConf</i> set to <b>NULL</b>, no handle is returned. This allows you to use the return status to determine if a configuration exists without the need to subsequently free the handle.

For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537921">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538041">CM_Free_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538046">CM_Free_Log_Conf_Handle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538529">CM_Get_First_Log_Conf_Ex</a>
 

 

