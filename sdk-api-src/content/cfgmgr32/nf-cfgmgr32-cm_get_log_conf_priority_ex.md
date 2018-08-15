---
UID: NF:cfgmgr32.CM_Get_Log_Conf_Priority_Ex
title: CM_Get_Log_Conf_Priority_Ex function
author: windows-sdk-content
description: The CM_Get_Log_Conf_Priority_Ex function obtains the configuration priority of a specified logical configuration on a local or a remote machine.
old-location: devinst\cm_get_log_conf_priority_ex.htm
old-project: devinst
ms.assetid: e02e8885-b459-4a70-9f0d-7765603e9dc4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CM_Get_Log_Conf_Priority_Ex, CM_Get_Log_Conf_Priority_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Log_Conf_Priority_Ex, cfgmgrfn_f4e7d475-18c7-4854-bff1-a484014f07ac.xml, devinst.cm_get_log_conf_priority_ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
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
 - CM_Get_Log_Conf_Priority_Ex
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_Log_Conf_Priority_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/0db6c2f4-2d44-49ad-a1cc-f29a5088c74c">CM_Get_Log_Conf_Priority</a> instead.]

The <b>CM_Get_Log_Conf_Priority_Ex</b> function obtains the configuration priority of a specified <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a> on a local or a remote machine.


## -parameters




### -param lcLogConf [in]

Caller-supplied handle to a logical configuration. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/9de0b04d-96be-4c93-b7af-09200fdcf807">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/7ef14797-ea67-40cb-ad8d-e8c846ae1fd4">CM_Get_First_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb562b5c-eb40-4be4-89a3-0e69a78ae6ea">CM_Get_First_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/fa256bda-a7ee-4583-a91b-e7c2ef39b3f2">CM_Get_Next_Log_Conf</a>



<a href="https://msdn.microsoft.com/590baeb8-9234-4895-a05b-1917b2ee0155">CM_Get_Next_Log_Conf_Ex</a>



### -param pPriority [out]

Caller-supplied address of a location to receive a configuration priority value. For a list of priority values, see the description of <i>Priority</i> for <a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Log_Conf_Priority_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/0db6c2f4-2d44-49ad-a1cc-f29a5088c74c">CM_Get_Log_Conf_Priority</a>
 

 

