---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# SetupDiGetDeviceInfoListDetailA function


## -description


The <b>SetupDiGetDeviceInfoListDetail</b> function retrieves information associated with a device information set including the class GUID, remote computer handle, and remote computer name.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which to retrieve information.


### -param DeviceInfoSetDetailData [out]

A pointer to a caller-initialized <a href="https://msdn.microsoft.com/library/windows/hardware/ff552345">SP_DEVINFO_LIST_DETAIL_DATA</a> structure that receives the device information set information. For more information about this structure, see the following <b>Remarks</b> section.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the parameters are valid, <b>SetupDiGetDeviceInfoListDetail</b> sets values in the <i>DeviceInfoSetDetailData</i> structure (except for the <b>cbSize</b> field) and returns status NO_ERROR. 

A caller of <b>SetupDiGetDeviceInfoListDetail</b> must set <i>DeviceInfoSetDetailData.</i><b>cbSize</b> to <b>sizeof</b>(SP_DEVINFO_LIST_DETAIL_DATA) or the function will fail and the call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> will return ERROR_INVALID_USER_BUFFER.

If <b>SetupDiGetDeviceInfoListDetail</b> completes successfully, <i>DeviceInfoSetDetailData.</i><b>ClassGuid</b> contains the class GUID associated with the device information set or a GUID_NULL structure.

If <b>SetupDiGetDeviceInfoListDetail</b> completes successfully and the device information set is for a remote system, <i>DeviceInfoSetDetailData.</i><b>RemoteMachineHandle</b> contains the ConfigMgr32 system handle for accessing the remote system and <i>DeviceInfoSetDetailData.</i><b>RemoteMachineName</b> contains the name of the remote system. If there is a remote handle for the device information set, it must be used when calling <b>CM_</b><i>Xxx</i><b>_Ex</b> functions because the DevInst handles are relative to the remote handle.

If the device information set is for the local computer, <i>DeviceInfoSetDetailData.</i><b>RemoteMachineHandle</b> is <b>NULL</b> and <i>DeviceInfoSetDetailData.</i><b>RemoteMachineName</b> is an empty string. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550958">SetupDiCreateDeviceInfoListEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551072">SetupDiGetClassDevsEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551101">SetupDiGetDeviceInfoListClass</a>
 

 

