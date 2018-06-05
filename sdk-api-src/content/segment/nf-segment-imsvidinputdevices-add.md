---
UID: NF:segment.IMSVidInputDevices.Add
title: IMSVidInputDevices::Add
author: windows-sdk-content
description: The Add method adds an input device to the collection.
old-location: mstv\imsvidinputdevices_add.htm
old-project: mstv
ms.assetid: b3a8ab2a-4b9c-41d2-9fb6-5862891eba42
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IMSVidInputDevices interface, IMSVidInputDevices interface [Microsoft TV Technologies],Add method, IMSVidInputDevices.Add, IMSVidInputDevices::Add, IMSVidInputDevicesAdd, mstv.imsvidinputdevices_add, segment/IMSVidInputDevices::Add
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidInputDevices.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidInputDevices::Add


## -description


The <b>Add</b> method adds an input device to the collection.


## -parameters




### -param pDB [in]

Pointer to the device's <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a> interface.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This collection is read-only; cannot add any items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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



<a href="https://msdn.microsoft.com/c8990564-70d3-4962-9ff2-24664dbc1161">IMSVidInputDevices::Remove</a>
 

 

