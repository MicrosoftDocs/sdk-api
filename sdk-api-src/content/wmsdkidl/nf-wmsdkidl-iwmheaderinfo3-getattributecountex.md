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

# IWMHeaderInfo3::GetAttributeCountEx


## -description



The <b>GetAttributeCountEx</b> method retrieves the total number of attributes associated with a specified stream number. You can also use this method to get the number of attributes not associated with a specific stream (file-level attributes), or to get the total number of attributes in the file, regardless of stream number.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which to retrieve the attribute count. Pass zero to retrieve the count of attributes that apply to the file rather than a specific stream. Pass 0xFFFF to retrieve the total count of all attributes in the file, both stream-specific and file-level.


### -param pcAttributes [out]

Pointer to a <b>WORD</b> containing the number of attributes that exist for the specified stream.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcAttributes</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number.

</td>
</tr>
</table>
 




## -remarks



The maximum number of attributes for a single stream is 65535, the capacity of the <b>WORD</b> parameter, <i>pcAttributes</i>. If you pass 0xFFFF as <i>wStreamNum</i>, this method will return the total number of attributes for the entire file. This number could potentially be greater than the capacity of <i>pcAttributes</i>. If the number of attributes in the file is greater than 65535, this method will produce unpredictable results. In reality, no file should ever have this many attributes. If your application makes use of an extremely large number of attributes, simply make individual calls to <b>GetAttributeCountEx</b> for each stream and for the file-level attributes.




## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

