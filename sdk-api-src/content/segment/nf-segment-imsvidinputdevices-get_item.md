---
UID: NF:segment.IMSVidInputDevices.get_Item
title: IMSVidInputDevices::get_Item
author: windows-driver-content
description: The get_Item method retrieves the specified item from the collection.
old-location: mstv\imsvidinputdevices_get_item.htm
old-project: mstv
ms.assetid: 4d8b2d88-e591-4280-966b-9c23f05d55f9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidInputDevices interface [Microsoft TV Technologies],get_Item method, IMSVidInputDevices.get_Item, IMSVidInputDevices::get_Item, IMSVidInputDevicesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IMSVidInputDevices interface, mstv.imsvidinputdevices_get_item, segment/IMSVidInputDevices::get_Item
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
-	IMSVidInputDevices.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidInputDevices::get_Item


## -description


The <b>get_Item</b> method retrieves the specified item from the collection.


## -parameters




### -param v [in]

<b>VARIANT</b> that specifies the index of the item to retrieve.


### -param pDB






#### - ppDB [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a> interface pointer.


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
The index is out of range.

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
Unexpected error.

</td>
</tr>
</table>
 




## -remarks



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <code>IMSVidInputDevices::get_Count() - 1</code>.

If the method succeeds, the <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices Interface</a>
 

 

