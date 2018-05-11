---
UID: NF:segment.IMSVidDevice.get_Category
title: IMSVidDevice::get_Category
author: windows-driver-content
description: The get_Category method retrieves the category of the device as a BSTR.
old-location: mstv\imsviddevice_get_category.htm
old-project: mstv
ms.assetid: 369080c6-b707-494e-a663-e78e7d8d3eaf
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_Category method, IMSVidDevice.get_Category, IMSVidDevice::get_Category, IMSVidDeviceget_Category, get_Category, get_Category method [Microsoft TV Technologies], get_Category method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_category, segment/IMSVidDevice::get_Category
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
-	IMSVidDevice.get_Category
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidDevice::get_Category


## -description


The <b>get_Category</b> method retrieves the category of the device as a <b>BSTR</b>.


## -parameters




### -param Guid






#### - pGuid [out]

<b>BSTR</b> that receives the device category.


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



The device category is identified by a <b>GUID</b>. This method returns a string representation of the <b>GUID</b>.

This method is provided for Automation clients. C++ applications can use the <a href="https://msdn.microsoft.com/2c5023ee-f38b-48c7-907d-363ca70bf94f">IMSVidDevice::get__Category</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

