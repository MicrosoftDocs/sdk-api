---
UID: NF:segment.IMSVidDevice.get_ClassID
title: IMSVidDevice::get_ClassID
author: windows-driver-content
description: The get_ClassID method retrieves the device's class identifier (CLSID) as a BSTR.
old-location: mstv\imsviddevice_get_classid.htm
old-project: mstv
ms.assetid: 78910e3d-bd00-48c5-b1be-504dc92280a0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],get_ClassID method, IMSVidDevice.get_ClassID, IMSVidDevice::get_ClassID, IMSVidDeviceget_ClassID, get_ClassID, get_ClassID method [Microsoft TV Technologies], get_ClassID method [Microsoft TV Technologies],IMSVidDevice interface, mstv.imsviddevice_get_classid, segment/IMSVidDevice::get_ClassID
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
-	IMSVidDevice.get_ClassID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidDevice::get_ClassID


## -description


The <b>get_ClassID</b> method retrieves the device's class identifier (CLSID) as a <b>BSTR</b>.


## -parameters




### -param Clsid






#### - pClsid [out]

Pointer to a variable that receives a string representation of the CLSID.


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



This method is provided for Automation clients. C++ applications can use the <a href="https://msdn.microsoft.com/80890372-2d92-4a3a-963f-2a6ca6632c52">IMSVidDevice::get__ClassID</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>
 

 

