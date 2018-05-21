---
UID: NF:cfgmgr32.CM_Get_Log_Conf_Priority
title: CM_Get_Log_Conf_Priority function
author: windows-driver-content
description: The CM_Get_Log_Conf_Priority function obtains the configuration priority of a specified logical configuration on the local machine.
old-location: devinst\cm_get_log_conf_priority.htm
old-project: devinst
ms.assetid: 0db6c2f4-2d44-49ad-a1cc-f29a5088c74c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CM_Get_Log_Conf_Priority, CM_Get_Log_Conf_Priority function [Device and Driver Installation], cfgmgr32/CM_Get_Log_Conf_Priority, cfgmgrfn_23c7a94b-fd43-493e-ae6b-56ce7c69278b.xml, devinst.cm_get_log_conf_priority
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
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Cfgmgr32.dll
api_name:
-	CM_Get_Log_Conf_Priority
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_Log_Conf_Priority function


## -description


The <b>CM_Get_Log_Conf_Priority</b> function obtains the configuration priority of a specified <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a> on the local machine.


## -parameters




### -param lcLogConf [in]

Caller-supplied handle to a logical configuration. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/library/windows/hardware/ff537921">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537926">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538522">CM_Get_First_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538529">CM_Get_First_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538591">CM_Get_Next_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538598">CM_Get_Next_Log_Conf_Ex</a>



### -param pPriority [out]

Caller-supplied address of a location to receive a configuration priority value. For a list of priority values, see the description of <i>Priority</i> for <a href="https://msdn.microsoft.com/library/windows/hardware/ff537921">CM_Add_Empty_Log_Conf</a>.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Log_Conf_Priority</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538585">CM_Get_Log_Conf_Priority_Ex</a>
 

 

