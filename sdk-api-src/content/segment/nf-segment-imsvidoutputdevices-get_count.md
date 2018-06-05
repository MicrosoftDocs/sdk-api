---
UID: NF:segment.IMSVidOutputDevices.get_Count
title: IMSVidOutputDevices::get_Count
author: windows-sdk-content
description: The get_Count method retrieves the number of items in the collection.
old-location: mstv\imsvidoutputdevices_get_count.htm
old-project: mstv
ms.assetid: c4da44cb-84cb-46ae-9898-993802c9bfac
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidOutputDevices interface [Microsoft TV Technologies],get_Count method, IMSVidOutputDevices.get_Count, IMSVidOutputDevices::get_Count, IMSVidOutputDevicesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IMSVidOutputDevices interface, mstv.imsvidoutputdevices_get_count, segment/IMSVidOutputDevices::get_Count
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
-	IMSVidOutputDevices.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidOutputDevices::get_Count


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




<a href="https://msdn.microsoft.com/54776225-ad60-450b-99b4-851cae60ffa7">IMSVidOutputDevices Interface</a>
 

 

