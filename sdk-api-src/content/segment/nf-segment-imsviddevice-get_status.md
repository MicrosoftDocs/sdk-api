---
UID: NF:segment.IMSVidDevice.get_Status
title: IMSVidDevice::get_Status
author: windows-driver-content
description: The get_Status method retrieves status information about the device.
old-location: mstv\imsviddevice_get_status.htm
old-project: mstv
ms.assetid: b11df7f3-d227-4c74-89a3-90716b3b3a12
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Status method, IMSVidDevice.get_Status, IMSVidDevice::get_Status, IMSVidDeviceget_Status, get_Status, get_Status method [Microsoft TV Technologies], get_Status method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_status, segment/IMSVidDevice::get_Status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidDevice.get_Status
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidDevice::get_Status


## -description


The <b>get_Status</b> method retrieves status information about the device.


## -parameters




### -param Status






#### - pStatus [out]

Pointer to a variable of that receives the current status.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks




        Not all device types implement this method.
      




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

