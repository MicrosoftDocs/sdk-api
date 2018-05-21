---
UID: NF:segment.IMSVidDevice.IsEqualDevice
title: IMSVidDevice::IsEqualDevice
author: windows-driver-content
description: The IsEqualDevice method queries whether this device and another device represent the same underlying hardware.
old-location: mstv\imsviddevice_isequaldevice.htm
old-project: mstv
ms.assetid: b0f59466-7a2a-453e-999c-c7ebf126d18b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],IsEqualDevice method, IMSVidDevice.IsEqualDevice, IMSVidDevice::IsEqualDevice, IMSVidDeviceIsEqualDevice, IsEqualDevice, IsEqualDevice method [Microsoft TV Technologies], IsEqualDevice method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_isequaldevice, segment/IMSVidDevice::IsEqualDevice
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
-	IMSVidDevice.IsEqualDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidDevice::IsEqualDevice


## -description


The <b>IsEqualDevice</b> method queries whether this device and another device represent the same underlying hardware.


## -parameters




### -param Device




### -param IsEqual






#### - pDevice [in]

Pointer to the other device's <a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a> interface.


#### - pIsEqual [out]

Pointer to a variable that receives one of the following values.

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
<td>VARIANT_TRUE</td>
<td>The two devices represent the same underlying hardware.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The two devices do not represent the same hardware.</td>
</tr>
</table>
 


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
Success; returned VARIANT_TRUE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Success; returned VARIANT_FALSE.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

