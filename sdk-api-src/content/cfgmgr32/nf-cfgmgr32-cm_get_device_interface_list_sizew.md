---
UID: NF:cfgmgr32.CM_Get_Device_Interface_List_SizeW
title: CM_Get_Device_Interface_List_SizeW function (cfgmgr32.h)
description: The CM_Get_Device_Interface_List_Size function retrieves the buffer size that must be passed to the CM_Get_Device_Interface_List function.helpviewer_keywords: ["CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES","CM_GET_DEVICE_INTERFACE_LIST_PRESENT","CM_Get_Device_Interface_List_Size","CM_Get_Device_Interface_List_Size function [Device and Driver Installation]","CM_Get_Device_Interface_List_SizeA","CM_Get_Device_Interface_List_SizeW","cfgmgr32/CM_Get_Device_Interface_List_Size","cfgmgr32/CM_Get_Device_Interface_List_SizeA","cfgmgr32/CM_Get_Device_Interface_List_SizeW","cfgmgrfn_91624b8d-408b-4b08-b23c-aecc2c4581d0.xml","devinst.cm_get_device_interface_list_size"]
old-location: devinst\cm_get_device_interface_list_size.htm
tech.root: devinst
ms.assetid: f3e1ceb7-9812-4339-889f-dade2efb3998
ms.date: 12/05/2018
ms.keywords: CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES, CM_GET_DEVICE_INTERFACE_LIST_PRESENT, CM_Get_Device_Interface_List_Size, CM_Get_Device_Interface_List_Size function [Device and Driver Installation], CM_Get_Device_Interface_List_SizeA, CM_Get_Device_Interface_List_SizeW, cfgmgr32/CM_Get_Device_Interface_List_Size, cfgmgr32/CM_Get_Device_Interface_List_SizeA, cfgmgr32/CM_Get_Device_Interface_List_SizeW, cfgmgrfn_91624b8d-408b-4b08-b23c-aecc2c4581d0.xml, devinst.cm_get_device_interface_list_size
f1_keywords:
- cfgmgr32/CM_Get_Device_Interface_List_Size
dev_langs:
- c++
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_Interface_List_SizeW (Unicode) and CM_Get_Device_Interface_List_SizeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- CfgMgr32.dll
- API-MS-Win-Devices-Config-L1-1-0.dll
- API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
- CM_Get_Device_Interface_List_Size
- CM_Get_Device_Interface_List_SizeA
- CM_Get_Device_Interface_List_SizeW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CM_Get_Device_Interface_List_SizeW function


## -description


The <b>CM_Get_Device_Interface_List_Size</b> function retrieves the buffer size 
     that must be passed to the 
     <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista">CM_Get_Device_Interface_List</a> 
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
           <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>. If specified, the 
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




<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista">CM_Get_Device_Interface_List</a>
 

 

