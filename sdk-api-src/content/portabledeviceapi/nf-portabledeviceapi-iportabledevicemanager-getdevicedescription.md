---
UID: NF:portabledeviceapi.IPortableDeviceManager.GetDeviceDescription
title: IPortableDeviceManager::GetDeviceDescription
author: windows-sdk-content
description: Retrieves the description of a device.
old-location: wpdsdk\iportabledevicemanager_getdevicedescription.htm
old-project: wpd_sdk
ms.assetid: 16c08c8a-9ce7-455a-9859-6b0be406f642
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDeviceDescription, GetDeviceDescription method [Windows Portable Devices SDK], GetDeviceDescription method [Windows Portable Devices SDK],IPortableDeviceManager interface, IPortableDeviceManager interface [Windows Portable Devices SDK],GetDeviceDescription method, IPortableDeviceManager.GetDeviceDescription, IPortableDeviceManager::GetDeviceDescription, IPortableDeviceManagerGetDeviceDescription, portabledeviceapi/IPortableDeviceManager::GetDeviceDescription, wpdsdk.iportabledevicemanager_getdevicedescription
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
 - IPortableDeviceManager.GetDeviceDescription
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceManager::GetDeviceDescription


## -description



Retrieves the description of a device.




## -parameters




### -param pszPnPDeviceID [in]

Pointer to a null-terminated string that contains the device's Plug and Play ID. You can retrieve a list of Plug and Play names of devices that are currently connected by calling <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">GetDevices</a>.


### -param pDeviceDescription [in, out]

A caller-allocated buffer to hold the user-description name of the device. The caller must allocate the memory for this parameter. To learn the required size for this parameter, first call this method with this parameter set to <b>NULL</b> and <i>pcchDeviceDescription</i> set to <b>0</b>; the method will succeed and set <i>pcchDeviceDescription</i> to the required buffer size to hold the device-friendly name, including the termination character.


### -param pcchDeviceDescription [in, out]

The number of characters (not including the termination character) in <i>pDeviceDescription</i>. On input, the maximum length of <i>pDeviceDescription</i>; on output, the length of the returned string in <i>pDeviceDescription</i>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">GetDevices</a>



<a href="https://msdn.microsoft.com/11cd5b2b-e8f8-4ba1-8527-f7a403f399d5">IPortableDeviceManager Interface</a>
 

 

