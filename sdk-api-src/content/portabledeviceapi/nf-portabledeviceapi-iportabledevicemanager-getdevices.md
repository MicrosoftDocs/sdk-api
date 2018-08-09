---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDevices
title: IPortableDeviceManager::GetDevices
author: windows-sdk-content
description: Retrieves a list of portable devices connected to the computer.
old-location: wpdsdk\iportabledevicemanager_getdevices.htm
old-project: wpd_sdk
ms.assetid: 5061b3c0-8b93-480d-b1c6-0a6b616a2c8d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDevices, GetDevices method [Windows Portable Devices SDK], GetDevices method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDevices method, IPortableDeviceManager.GetDevices, IPortableDeviceManager::GetDevices, IPortableDeviceManagerGetDevices, portabledeviceapi/IPortableDeviceManager::GetDevices, wpdsdk.iportabledevicemanager_getdevices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceManager.GetDevices
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceManager::GetDevices


## -description



Retrieves a list of portable devices connected to the computer.




## -parameters




### -param pPnPDeviceIDs [in, out]

A caller-allocated array of string pointers that holds the Plug and Play names of all of the connected devices. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcPnPDeviceIDs</i> set to zero, and then allocate a buffer according to the value retrieved by <i>pcPnPDeviceIDs</i>. These names can be used by <a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">IPortableDevice::Open</a> to create a connection to a device.


### -param pcPnPDeviceIDs [in, out]

On input, the number of values that <i>pPnPDeviceIDs</i> can hold. On output, a pointer to the number of devices actually written to <i>pPnPDeviceIDs</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPnPDeviceIDs</i> buffer is too small to hold all the values requested, but <i>pcPnPDeviceIDs</i> values have been written to <i>pPnPDeviceIDs</i>.

</td>
</tr>
</table>
 




## -remarks



The list of devices is generated when the device manager is instantiated; it does not refresh as devices connect and disconnect. To refresh the list of connected devices, call <a href="https://msdn.microsoft.com/89163407-7b38-4c79-8171-67a5b7e1d17c">RefreshDeviceList</a>.

The API allocates the memory for each string pointed to by the <i>pPnPDeviceIDs</i> array. Once your application no longer needs these strings, it must iterate through this array and free the associated memory by calling the <b>CoTaskMemFree</b> function.


#### Examples

For an example of how to use this method to enumerate devices, see <a href="https://msdn.microsoft.com/28ded3cf-b0c8-4c90-ab39-efc879adb6e7">Enumerating Devices</a>. For an example of how to use this method to enumerate Services, see <a href="https://msdn.microsoft.com/6ee6eecb-3812-45c6-8b27-7dfd6fa82758">Enumerating Services</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/28ded3cf-b0c8-4c90-ab39-efc879adb6e7">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/6ee6eecb-3812-45c6-8b27-7dfd6fa82758">Enumerating Services</a>



<a href="https://msdn.microsoft.com/11cd5b2b-e8f8-4ba1-8527-f7a403f399d5">IPortableDeviceManager Interface</a>
 

 

