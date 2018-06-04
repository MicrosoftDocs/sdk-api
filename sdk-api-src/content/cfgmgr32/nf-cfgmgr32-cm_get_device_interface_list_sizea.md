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

# CM_Get_Device_Interface_List_SizeA function


## -description


The <b>CM_Get_Device_Interface_List_Size</b> function retrieves the buffer size 
     that must be passed to the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff538463">CM_Get_Device_Interface_List</a> 
     function.


## -parameters




### -param pulLen [out]

Caller-supplied pointer to a location that receives the required length, in characters, of a buffer to 
           hold the multiple Unicode strings that will be returned by 
           <b>CM_Get_Device_Interface_List</b>.


### -param InterfaceClassGuid [in]

Supplies a GUID that identifies a 
           <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a>.


### -param pDeviceID [in, optional]

Caller-supplied pointer to a NULL-terminated string that represents a 
           <a href="devinst.device_instance_ids">device instance ID</a>. If specified, the 
           function retrieves the length of symbolic link names for the device interfaces that are supported by the 
           device, for the specified class. If this value is <b>NULL</b>, or if it points to a 
           zero-length string, the function retrieves the length of symbolic link names for all interfaces that belong 
           to the specified class.


### -param ulFlags [in]

Contains one of the following caller-supplied flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES"></a><a id="cm_get_device_interface_list_all_devices"></a><dl>
<dt><b>CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES</b></dt>
</dl>
</td>
<td width="60%">
The function provides the size of a list that contains device interfaces associated with all devices 
             that match the specified <b>GUID</b> and device instance ID, if any.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_GET_DEVICE_INTERFACE_LIST_PRESENT"></a><a id="cm_get_device_interface_list_present"></a><dl>
<dt><b>CM_GET_DEVICE_INTERFACE_LIST_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The function provides the size of a list containing device interfaces associated with devices that 
             are currently active, and which match the specified GUID and device instance ID, if any.

</td>
</tr>
</table>
 


## -returns



If the operation succeeds, the function returns <b>CR_SUCCESS</b>. Otherwise, it 
           returns one of the error codes with the <b>CR_</b> prefix as defined in 
           Cfgmgr32.h.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538463">CM_Get_Device_Interface_List</a>
 

 

