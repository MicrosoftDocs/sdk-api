---
UID: NF:segment.IMSVidInputDevice.IsViewable
title: IMSVidInputDevice::IsViewable
author: windows-sdk-content
description: The IsViewable method determines whether this device can view the specified tune request.
old-location: mstv\imsvidinputdevice_isviewable.htm
tech.root: MSTV
ms.assetid: 4f62bcc4-8c58-4663-9b1f-a5ed7d000a79
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidInputDevice interface [Microsoft TV Technologies],IsViewable method, IMSVidInputDevice.IsViewable, IMSVidInputDevice::IsViewable, IMSVidInputDeviceIsViewable, IsViewable, IsViewable method [Microsoft TV Technologies], IsViewable method [Microsoft TV Technologies],IMSVidInputDevice interface, mstv.imsvidinputdevice_isviewable, segment/IMSVidInputDevice::IsViewable
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
 - IMSVidInputDevice.IsViewable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidInputDevice.IsViewable
: 
---

# IMSVidInputDevice::IsViewable


## -description


The <b>IsViewable</b> method determines whether this device can view the specified tune request.

Currently this method is not implemented by any of the supported input devices.


## -parameters




### -param v

TBD


### -param pfViewable [out]

Pointer to variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The device can view this tune request.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The device cannot view this tune request.</td>
</tr>
</table>
 


#### - pv [in]

Specifies the tune request as a <b>VARIANT</b> type.


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
 




## -see-also




<a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice Interface</a>
 

 

