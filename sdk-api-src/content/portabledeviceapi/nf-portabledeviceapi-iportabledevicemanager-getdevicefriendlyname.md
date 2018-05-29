---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDeviceFriendlyName
title: IPortableDeviceManager::GetDeviceFriendlyName
author: windows-sdk-content
description: Retrieves the user-friendly name for the device.
old-location: wpdsdk\iportabledevicemanager_getdevicefriendlyname.htm
old-project: wpd_sdk
ms.assetid: 589995bb-fcce-412e-8828-a84e5809af2b
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: GetDeviceFriendlyName, GetDeviceFriendlyName method [Windows Portable Devices SDK], GetDeviceFriendlyName method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDeviceFriendlyName method, IPortableDeviceManager.GetDeviceFriendlyName, IPortableDeviceManager::GetDeviceFriendlyName, IPortableDeviceManagerGetDeviceFriendlyName, portabledeviceapi/IPortableDeviceManager::GetDeviceFriendlyName, wpdsdk.iportabledevicemanager_getdevicefriendlyname
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceManager.GetDeviceFriendlyName
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceManager::GetDeviceFriendlyName


## -description



Retrieves the user-friendly name for the device.




## -parameters




### -param pszPnPDeviceID [in]

Pointer to a null-terminated string that contains the device's Plug and Play ID. You can retrieve a list of Plug and Play names of all devices that are connected to the computer by calling <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">GetDevices</a>.


### -param pDeviceFriendlyName [in, out]

A caller-allocated buffer that is used to hold the user-friendly name for the device. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcchDeviceFriendlyName</i> set to <b>0</b>; the method will succeed and set <i>pcchDeviceFriendlyName</i> to the required buffer size to hold the device-friendly name, including the termination character.


### -param pcchDeviceFriendlyName [in, out]

On input, the maximum number of characters that <i>pDeviceFriendlyName</i> can hold, not including the termination character. On output, the number of characters that is returned by <i>pDeviceFriendlyName</i>, not including the termination character.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is not large enough to hold the device description. (Refer to the value returned in <i>pcchDeviceDescription</i> for the required size.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The device description could not be found.

</td>
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
</table>
 




## -remarks



A device is not required to support this method. If this method fails to retrieve a name, try requesting the <a href="object_properties.htm">WPD_OBJECT_NAME</a> property of the device object (the object with the ID WPD_DEVICE_OBJECT_ID).




## -see-also




<a href="https://msdn.microsoft.com/11cd5b2b-e8f8-4ba1-8527-f7a403f399d5">IPortableDeviceManager Interface</a>



<a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a>
 

 

