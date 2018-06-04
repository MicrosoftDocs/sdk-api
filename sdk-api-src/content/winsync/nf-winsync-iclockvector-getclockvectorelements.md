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

# IClockVector::GetClockVectorElements


## -description


Returns an enumerator that iterates through the clock vector elements.


## -parameters




### -param riid [in]

The IID of the enumeration interface that is requested. Must be either <b>IID_IEnumClockVector</b> or <b>IID_IEnumFeedClockVector</b>.


### -param ppiEnumClockVector [out]

Returns an object that implements <i>riid</i> and that can enumerate the clock vector elements.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
<i>riid</i> is not  <b>IID_IEnumClockVector</b> or <b>IID_IEnumFeedClockVector</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/31aef38d-a6df-4645-a192-9145d3ec90ad">IClockVector Interface</a>
 

 

