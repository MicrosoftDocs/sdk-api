---
UID: NF:segment.IMSVidAudioRendererDevices.Remove
title: IMSVidAudioRendererDevices::Remove
author: windows-sdk-content
description: The Remove method removes an item from the collection.
old-location: mstv\imsvidaudiorendererdevices_remove.htm
tech.root: mstv
ms.assetid: 5a9cf752-e3f8-40bf-89e8-e223654e4080
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidAudioRendererDevices interface [Microsoft TV Technologies],Remove method, IMSVidAudioRendererDevices.Remove, IMSVidAudioRendererDevices::Remove, IMSVidAudioRendererDevicesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IMSVidAudioRendererDevices interface, mstv.imsvidaudiorendererdevices_remove, segment/IMSVidAudioRendererDevices::Remove
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
 - IMSVidAudioRendererDevices.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidAudioRendererDevices::Remove


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only; cannot remove any items.

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



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <a href="https://msdn.microsoft.com/en-us/library/Dd694438(v=VS.85).aspx">IMSVidAudioRendererDevices::get_Count</a> - 1.




## -see-also




<a href="https://msdn.microsoft.com/2cf03260-7abe-4602-8364-447d076a4f76">IMSVidAudioRendererDevices Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694437(v=VS.85).aspx">IMSVidAudioRendererDevices::Add</a>
 

 

