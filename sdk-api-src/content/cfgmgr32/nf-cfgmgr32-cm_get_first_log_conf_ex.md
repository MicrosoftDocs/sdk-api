---
UID: NF:cfgmgr32.CM_Get_First_Log_Conf_Ex
title: CM_Get_First_Log_Conf_Ex function
author: windows-sdk-content
description: The CM_Get_First_Log_Conf_Ex function obtains the first logical configuration associated with a specified device instance on a local or a remote machine.
old-location: devinst\cm_get_first_log_conf_ex.htm
tech.root: devinst
ms.assetid: cb562b5c-eb40-4be4-89a3-0e69a78ae6ea
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CM_Get_First_Log_Conf_Ex, CM_Get_First_Log_Conf_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_First_Log_Conf_Ex, cfgmgrfn_bfb585c9-0dba-4c24-991e-2e866e3e6e9b.xml, devinst.cm_get_first_log_conf_ex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_First_Log_Conf_Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_First_Log_Conf_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/7ef14797-ea67-40cb-ad8d-e8c846ae1fd4">CM_Get_First_Log_Conf</a> instead.]

The <b>CM_Get_First_Log_Conf_Ex</b> function obtains the first <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a> associated with a specified <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on a local or a remote machine.


## -parameters




### -param plcLogConf [out, optional]

Address of a location to receive the handle to a logical configuration, or <b>NULL</b>. See the <b>Remarks</b> section.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.


### -param ulFlags [in]

Caller-supplied flag value indicating the type of logical configuration being requested. For a list of flags, see the <i>ulFlags</i> description for <a href="https://msdn.microsoft.com/7ef14797-ea67-40cb-ad8d-e8c846ae1fd4">CM_Get_First_Log_Conf</a>.


### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_First_Log_Conf_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Calling <a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a> or <a href="https://msdn.microsoft.com/dd19400b-e83e-4feb-a968-b57656c9996c">CM_Free_Log_Conf_Ex</a> can invalidate the handle obtained from a previous call to <b>CM_Get_First_Log_Conf_Ex</b>. Thus if you want to obtain logical configurations after calling <b>CM_Add_Empty_Log_Conf_Ex</b> or <b>CM_Free_Log_Conf_Ex</b>, your code must call <b>CM_Get_First_Log_Conf_Ex</b> again and start at the first configuration.

The handle received in <i>plcLogConf</i> must be explicitly freed by calling <a href="https://msdn.microsoft.com/dd8a4a2a-9f99-48c0-acb6-e5ceed63c88e">CM_Free_Log_Conf_Handle</a>.

If <b>CM_Get_First_Log_Conf_Ex</b> is called with <i>plcLogConf</i> set to <b>NULL</b>, no handle is returned. This allows you to use the return status to determine if a configuration exists without the need to subsequently free the handle.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/dd19400b-e83e-4feb-a968-b57656c9996c">CM_Free_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/dd8a4a2a-9f99-48c0-acb6-e5ceed63c88e">CM_Free_Log_Conf_Handle</a>



<a href="https://msdn.microsoft.com/bcd46252-6f87-4d49-a24c-81789b0148d9">CM_Get_Child_Ex</a>



<b>CM_Get_First_Log_Conf</b>
 

 

