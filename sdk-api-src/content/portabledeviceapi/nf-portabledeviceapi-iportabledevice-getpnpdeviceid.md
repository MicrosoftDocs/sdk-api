---
UID: NF:portabledeviceapi.IPortableDevice.GetPnPDeviceID
title: IPortableDevice::GetPnPDeviceID method
author: windows-driver-content
description: The GetPnPDeviceID method retrieves the Plug and Play (PnP) device identifier that the application used to open the device.
old-location: wpdsdk\iportabledevice_getpnpdeviceid.htm
old-project: wpd_sdk
ms.assetid: e6bde2ac-ceef-47f8-b60b-e61595078e8c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPnPDeviceID method [Windows Portable Devices SDK], GetPnPDeviceID method [Windows Portable Devices SDK], IPortableDevice interface, GetPnPDeviceID,IPortableDevice.GetPnPDeviceID, IPortableDevice, IPortableDevice interface [Windows Portable Devices SDK], GetPnPDeviceID method, IPortableDevice::GetPnPDeviceID, IPortableDeviceGetPnPDeviceID, portabledeviceapi/IPortableDevice::GetPnPDeviceID, wpdsdk.iportabledevice_getpnpdeviceid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevice.GetPnPDeviceID
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDevice::GetPnPDeviceID method


## -description



        The <b>GetPnPDeviceID</b> method retrieves the Plug and Play (PnP) device identifier that the application used to open the device.
      


## -parameters




### -param ppszPnPDeviceID [out]


            Pointer to a null-terminated string that contains the Plug and Play ID string for the device.
          


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
<dt><b>E_WPD_DEVICE_NOT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">IPortableDevice::Open</a> method has not been called yet for this device.

</td>
</tr>
</table>
 




## -remarks




        After the application is through using the string returned by this method, it must call the <a href="4fe971c6-8611-453d-b69b-f02c17cf17d4">CoTaskMemFree</a> function to free the string.
      


        The <i>ppszPnPDeviceID</i> argument must not be set to <b>NULL</b>.
      




## -see-also




<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>



<a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">IPortableDevice::Open</a>
 

 

