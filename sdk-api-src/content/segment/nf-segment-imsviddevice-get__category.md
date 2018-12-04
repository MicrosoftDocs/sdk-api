---
UID: NF:segment.IMSVidDevice.get__Category
title: IMSVidDevice::get__Category
author: windows-sdk-content
description: The get__Category method retrieves the category of the device as a GUID.
old-location: mstv\imsviddevice_get__category.htm
tech.root: mstv
ms.assetid: 2c5023ee-f38b-48c7-907d-363ca70bf94f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get__Category method, IMSVidDevice.get__Category, IMSVidDevice::get__Category, IMSVidDeviceget__Category, get__Category, get__Category method [Microsoft TV Technologies], get__Category method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get__category, segment/IMSVidDevice::get__Category
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
 - IMSVidDevice.get__Category
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidDevice::get__Category


## -description


The <b>get__Category</b> method retrieves the category of the device as a <b>GUID</b>.


## -parameters




### -param Guid [out]

Pointer to a variable of type <b>GUID</b> that receives the device category.


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
 




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

