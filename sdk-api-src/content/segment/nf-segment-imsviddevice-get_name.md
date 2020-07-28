---
UID: NF:segment.IMSVidDevice.get_Name
title: IMSVidDevice::get_Name (segment.h)
description: The get_Name method retrieves the friendly name of the device.
helpviewer_keywords: ["IMSVidDevice interface [Microsoft TV Technologies]","get_Name method","IMSVidDevice.get_Name","IMSVidDevice::get_Name","IMSVidDeviceget_Name","get_Name","get_Name method [Microsoft TV Technologies]","get_Name method [Microsoft TV Technologies]","IMSVidDevice interface","mstv.imsviddevice_get_name","segment/IMSVidDevice::get_Name"]
old-location: mstv\imsviddevice_get_name.htm
tech.root: mstv
ms.assetid: eb484684-7c20-498d-939e-ae5964d35669
ms.date: 12/05/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Name method, IMSVidDevice.get_Name, IMSVidDevice::get_Name, IMSVidDeviceget_Name, get_Name, get_Name method [Microsoft TV Technologies], get_Name method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_name, segment/IMSVidDevice::get_Name
f1_keywords:
- segment/IMSVidDevice.get_Name
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidDevice.get_Name
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidDevice::get_Name


## -description


The <b>get_Name</b> method retrieves the friendly name of the device.


## -parameters




### -param Name [out]

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




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice Interface</a>
 

 

