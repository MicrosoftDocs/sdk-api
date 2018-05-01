---
UID: NF:segment.IMSVidInputDevices.get_Count
title: IMSVidInputDevices::get_Count method
author: windows-driver-content
description: The get_Count method retrieves the number of items in the collection.
old-location: mstv\imsvidinputdevices_get_count.htm
old-project: mstv
ms.assetid: 52c2d9a1-f688-4f5e-a120-082d70f8dff1
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidInputDevices, IMSVidInputDevices interface [Microsoft TV Technologies], get_Count method, IMSVidInputDevices::get_Count, IMSVidInputDevicesget_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies], IMSVidInputDevices interface, get_Count,IMSVidInputDevices.get_Count, mstv.imsvidinputdevices_get_count, segment/IMSVidInputDevices::get_Count
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
-	IMSVidInputDevices.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidInputDevices::get_Count method


## -description


The <b>get_Count</b> method retrieves the number of items in the collection.


## -parameters




### -param lCount






#### - plCount [out]

Pointer to a variable that receives the number of items.


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




<a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices Interface</a>
 

 

