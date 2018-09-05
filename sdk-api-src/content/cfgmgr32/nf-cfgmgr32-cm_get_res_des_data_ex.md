---
UID: NF:cfgmgr32.CM_Get_Res_Des_Data_Ex
title: CM_Get_Res_Des_Data_Ex function
author: windows-sdk-content
description: The CM_Get_Res_Des_Data_Ex function retrieves the information stored in a resource descriptor on a local or a remote machine.
old-location: devinst\cm_get_res_des_data_ex.htm
old-project: devinst
ms.assetid: fc7dc2d6-f4ef-4da7-af51-92053afa8db9
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CM_Get_Res_Des_Data_Ex, CM_Get_Res_Des_Data_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Res_Des_Data_Ex, cfgmgrfn_58308b51-6217-4e1e-80ac-b4d3b431cdfb.xml, devinst.cm_get_res_des_data_ex
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
 - CM_Get_Res_Des_Data_Ex
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_Res_Des_Data_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/f35975ac-022e-4e7c-a331-da0ccd0440a1">CM_Get_Res_Des_Data</a> instead.]

The <b>CM_Get_Res_Des_Data_Ex</b> function retrieves the information stored in a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> on a local or a remote machine.


## -parameters




### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="https://msdn.microsoft.com/91e9a686-2465-4ae8-9cc2-391cd98c2138">CM_Get_Next_Res_Des_Ex</a>.


### -param Buffer [out]

Address of a buffer to receive the contents of a resource descriptor. The required buffer size should be obtained by calling <a href="https://msdn.microsoft.com/59b96655-aea9-4f98-9f6a-1a9093db9c63">CM_Get_Res_Des_Data_Size_Ex</a>.


### -param BufferLen [in]

Caller-supplied length of the buffer specified by <i>Buffer</i>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Information returned in the buffer supplied by <i>Buffer</i> will be formatted as one of the resource type structures listed in the description of <a href="https://msdn.microsoft.com/f19996ae-f243-4e8c-b200-7d11c06490c9">CM_Add_Res_Des_Ex</a>, based on the resource type that was specified when <a href="https://msdn.microsoft.com/91e9a686-2465-4ae8-9cc2-391cd98c2138">CM_Get_Next_Res_Des_Ex</a> was called to obtain the resource descriptor handle.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/f35975ac-022e-4e7c-a331-da0ccd0440a1">CM_Get_Res_Des_Data</a>
 

 

