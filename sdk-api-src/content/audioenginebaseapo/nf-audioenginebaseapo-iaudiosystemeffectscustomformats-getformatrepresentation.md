---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAudioSystemEffectsCustomFormats::GetFormatRepresentation


## -description


The <code>GetFormatRepresentation</code> method retrieves a string representation of the custom format so that it can be displayed on a user-interface.


## -parameters




### -param nFormat [in]

Specifies the index of a supported format. This parameter can be any value in the range from zero to one less than the return value of <a href="https://msdn.microsoft.com/70d215e5-e30a-4fbd-b9c3-c988c6bbd941">GetFormatCount</a>. In other words, any value in the range from zero to GetFormatCount( ) - 1.


### -param ppwstrFormatRep [out, optional]

Specifies the address of the buffer that receives a NULL-terminated Unicode string that describes the custom format.


## -returns



The <code>GetFormatRepresentation</code> method returns S_OK when the call is successful. Otherwise, it returns one of the error codes shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed to function

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Return buffer cannot be allocated

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
nFormat is out of range

</td>
</tr>
</table>
 




## -remarks



The sAPO uses <a href="http://go.microsoft.com/fwlink/p/?linkid=154375">CoTaskMemAlloc</a> to allocate the returned string. The caller must use <a href="http://go.microsoft.com/fwlink/p/?linkid=154376">CoTaskMemFree</a> to delete the buffer that is pointed to by the <i>ppwstrFormatRep</i> parameter. 




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=154375">CoTaskMemAlloc</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=154376">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/70d215e5-e30a-4fbd-b9c3-c988c6bbd941">GetFormatCount</a>
 

 

