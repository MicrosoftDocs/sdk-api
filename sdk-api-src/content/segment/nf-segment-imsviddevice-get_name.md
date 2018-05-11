---
UID: NF:segment.IMSVidDevice.get_Name
title: IMSVidDevice::get_Name
author: windows-driver-content
description: The get_Name method retrieves the friendly name of the device.
old-location: mstv\imsviddevice_get_name.htm
old-project: mstv
ms.assetid: eb484684-7c20-498d-939e-ae5964d35669
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Name method, IMSVidDevice.get_Name, IMSVidDevice::get_Name, IMSVidDeviceget_Name, get_Name, get_Name method [Microsoft TV Technologies], get_Name method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_name, segment/IMSVidDevice::get_Name
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
-	IMSVidDevice.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidDevice::get_Name


## -description


The <b>get_Name</b> method retrieves the friendly name of the device.


## -parameters




### -param Name






#### - pName [out]

Pointer to a variable that receives the friendly name.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks




        The caller must free the returned string, using the <b>SysFreeString</b> function.
      




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

