---
UID: NF:segment.IMSVidVideoRendererDevices.get_Item
title: IMSVidVideoRendererDevices::get_Item
author: windows-driver-content
description: The get_Item method retrieves the specified item from the collection.
old-location: mstv\imsvidvideorendererdevices_get_item.htm
old-project: mstv
ms.assetid: 2cb169d2-f6b2-4156-aa11-f9b47437b731
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidVideoRendererDevices interface [Microsoft TV Technologies],get_Item method, IMSVidVideoRendererDevices.get_Item, IMSVidVideoRendererDevices::get_Item, IMSVidVideoRendererDevicesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, mstv.imsvidvideorendererdevices_get_item, segment/IMSVidVideoRendererDevices::get_Item
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
-	IMSVidVideoRendererDevices.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRendererDevices::get_Item


## -description


The <b>get_Item</b> method retrieves the specified item from the collection.


## -parameters




### -param v [in]

<b>VARIANT</b> that specifies the index of the item to retrieve.


### -param pDB






#### - ppDB [out]

Receives an <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface pointer. The caller must release the interface.


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



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <a href="https://msdn.microsoft.com/4308ed6a-b9c4-46f3-98eb-be23cd49c7dc">IMSVidVideoRendererDevices::get_Count</a> - 1.




## -see-also




<a href="https://msdn.microsoft.com/cf8e1307-b4a5-464b-b9a6-32c195941309">IMSVidVideoRendererDevices Interface</a>
 

 

