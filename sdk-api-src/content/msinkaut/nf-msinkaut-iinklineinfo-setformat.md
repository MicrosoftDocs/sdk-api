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

# IInkLineInfo::SetFormat


## -description



Specifies the display properties to set on the text ink object (tInk).




## -parameters




### -param pim [in]

A pointer to an <a href="https://msdn.microsoft.com/27d56034-725d-4b05-9c43-6b3180d7411b">INKMETRIC</a> structure which contains the display properties to set on the text ink object.


## -returns



This method can return one of these values.

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
The <i>pim</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the operation. The display properties are not changed.

</td>
</tr>
</table>
 




## -remarks



If the IMF_FONT_SELECTED_IN_HDC flag is set in the <i>pim</i> parameter, then the properties of the device context are applied to the ink; otherwise, the <a href="https://msdn.microsoft.com/27d56034-725d-4b05-9c43-6b3180d7411b">INKMETRIC</a> settings of the text ink object are applied.




## -see-also




<a href="https://msdn.microsoft.com/8f894963-7075-46f4-8809-82d1aa7e13e7">GetFormat Method</a>



<a href="https://msdn.microsoft.com/0082b7d3-61b2-478a-a6dd-ba59c20b7e1d">GetInkExtent Method</a>



<a href="https://msdn.microsoft.com/58774f49-6af2-4b81-bbd5-709eb694af2d">IInkLineInfo</a>



<a href="https://msdn.microsoft.com/27d56034-725d-4b05-9c43-6b3180d7411b">INKMETRIC Structure</a>
 

 

