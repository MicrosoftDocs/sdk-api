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

# IBDA_NameValueService::GetValueNameByIndex


## -description


Gets a name, specified by index, from the device's list of name/value pairs.


## -parameters




### -param ulIndex [in]

The zero-based index of the name to get.


### -param pbstrName [out]

Receives the name as a <b>BSTR</b>. The caller must free the <b>BSTR</b> by calling <b>SysFreeString</b>.


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
<dt><b>BDA_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulIndex</i> parameter is out of bounds.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7b6a12d2-24e4-42d8-9138-86c2fe558d86">IBDA_NameValueService</a>
 

 

