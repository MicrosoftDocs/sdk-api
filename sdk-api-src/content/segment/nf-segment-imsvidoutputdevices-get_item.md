---
UID: NF:segment.IMSVidOutputDevices.get_Item
title: IMSVidOutputDevices::get_Item
author: windows-driver-content
description: The get_Item method retrieves the specified item from the collection.
old-location: mstv\imsvidoutputdevices_get_item.htm
old-project: mstv
ms.assetid: 373dd785-3671-4afa-92ac-e61a39a68228
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidOutputDevices interface [Microsoft TV Technologies],get_Item method, IMSVidOutputDevices.get_Item, IMSVidOutputDevices::get_Item, IMSVidOutputDevicesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IMSVidOutputDevices interface, mstv.imsvidoutputdevices_get_item, segment/IMSVidOutputDevices::get_Item
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
-	IMSVidOutputDevices.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidOutputDevices::get_Item


## -description


The <b>get_Item</b> method retrieves the specified item from the collection.


## -parameters




### -param v [in]

<b>VARIANT</b> that specifies the index of the item to retrieve.


### -param pDB






#### - ppDB [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a> interface pointer.


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



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <code>IMSVidOutputDevices::get_Count - 1</code>.

If the method succeeds, the <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/54776225-ad60-450b-99b4-851cae60ffa7">IMSVidOutputDevices Interface</a>
 

 

