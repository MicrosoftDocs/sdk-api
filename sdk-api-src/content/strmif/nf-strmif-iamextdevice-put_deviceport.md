---
UID: NF:strmif.IAMExtDevice.put_DevicePort
title: IAMExtDevice::put_DevicePort
author: windows-driver-content
description: The put_DevicePort method assigns the communication port to which the external device is connected.
old-location: dshow\iamextdevice_put_deviceport.htm
old-project: DirectShow
ms.assetid: bb83ae40-875b-47c4-8e8e-944392ad0782
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMExtDevice interface [DirectShow],put_DevicePort method, IAMExtDevice.put_DevicePort, IAMExtDevice::put_DevicePort, IAMExtDeviceput_DevicePort, dshow.iamextdevice_put_deviceport, put_DevicePort, put_DevicePort method [DirectShow], put_DevicePort method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::put_DevicePort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtDevice.put_DevicePort
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtDevice::put_DevicePort


## -description



The <code>put_DevicePort</code> method assigns the communication port to which the external device is connected.



This method is not implemented.


## -parameters




### -param DevicePort [in]

Specifies the port to which the device will connect. Use one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>DEV_PORT_1394</td>
<td>IEEE 1394 Bus</td>
</tr>
<tr>
<td>DEV_PORT_ARTI</td>
<td>ARTI driver</td>
</tr>
<tr>
<td>DEV_PORT_COM1</td>
<td>COM1</td>
</tr>
<tr>
<td>DEV_PORT_COM2</td>
<td>COM2</td>
</tr>
<tr>
<td>DEV_PORT_COM3</td>
<td>COM3</td>
</tr>
<tr>
<td>DEV_PORT_COM4</td>
<td>COM4</td>
</tr>
<tr>
<td>DEV_PORT_DIAQ</td>
<td>Diaquest driver</td>
</tr>
<tr>
<td>DEV_PORT_MIN</td>
<td>DEV_PORT_SIM</td>
</tr>
<tr>
<td>DEV_PORT_SIM</td>
<td>Simulation port (used for "no hardware" simulation)</td>
</tr>
<tr>
<td>DEV_PORT_USB</td>
<td>Universal serial bus</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>



<a href="https://msdn.microsoft.com/307ad6ee-1084-4a83-bb19-f766f2328a0d">IAMExtDevice::get_DevicePort</a>
 

 

