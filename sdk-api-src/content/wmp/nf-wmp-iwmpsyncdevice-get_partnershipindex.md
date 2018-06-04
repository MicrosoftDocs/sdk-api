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

# IWMPSyncDevice::get_partnershipIndex


## -description



The <b>get_partnershipIndex</b> method retrieves the index of the device partnership.




## -parameters




### -param plIndex [out]

Pointer to a <b>long</b> that contains the partnership index value. Possible values range from 0 to 16.


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
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>
 




## -remarks



Windows Media Player 10 or later supports up to 16 device partnerships, numbered 1 to 16. The Player allows one partnership with one computer for each device. Creating a new partnership destroys any existing partnership with the current device.

When <i>plIndex</i> equals zero, no partnership exists.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/734a8717-3b7f-4a40-895f-b55cfabd665c">IWMPSyncDevice::createPartnership</a>



<a href="https://msdn.microsoft.com/ecb525b4-c804-47e6-8d6c-7d943010077a">IWMPSyncDevice::deletePartnership</a>



<a href="https://msdn.microsoft.com/36d40dc4-5641-49dd-9ef4-31d2acd0f41d">IWMPSyncDevice::get_deviceId</a>
 

 

