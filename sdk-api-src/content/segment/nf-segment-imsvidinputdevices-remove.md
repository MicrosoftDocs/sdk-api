---
UID: NF:segment.IMSVidInputDevices.Remove
title: IMSVidInputDevices::Remove method
author: windows-driver-content
description: The Remove method removes an item from the collection.
old-location: mstv\imsvidinputdevices_remove.htm
old-project: mstv
ms.assetid: c8990564-70d3-4962-9ff2-24664dbc1161
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidInputDevices, IMSVidInputDevices interface [Microsoft TV Technologies], Remove method, IMSVidInputDevices::Remove, IMSVidInputDevicesRemove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies], IMSVidInputDevices interface, Remove,IMSVidInputDevices.Remove, mstv.imsvidinputdevices_remove, segment/IMSVidInputDevices::Remove
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
-	IMSVidInputDevices.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidInputDevices::Remove method


## -description


The <b>Remove</b> method removes an item from the collection.


## -parameters




### -param v [in]

<b>VARIANT</b> that specifies the index of the item to remove.


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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Wrong <b>VARIANT</b> type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This collection is read-only; no items can be removed from it

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>
 




## -remarks



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <a href="https://msdn.microsoft.com/52c2d9a1-f688-4f5e-a120-082d70f8dff1">IMSVidInputDevices::get_Count</a> - 1.




## -see-also




<a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices Interface</a>



<a href="https://msdn.microsoft.com/b3a8ab2a-4b9c-41d2-9fb6-5862891eba42">IMSVidInputDevices::Add</a>
 

 

