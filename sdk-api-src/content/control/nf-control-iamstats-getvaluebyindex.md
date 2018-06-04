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

# IAMStats::GetValueByIndex


## -description



The <code>GetValueByIndex</code> method retrieves a statistic, by index.




## -parameters




### -param lIndex [in]

Zero-based index of the statistic.


### -param szName [out]

Pointer to a variable that receives the name of the statistic.


### -param lCount [out]

Pointer to a variable that receives the number of values that were recorded.


### -param dLast [out]

Pointer to a variable that receives the most recent value that was recorded.


### -param dAverage [out]

Pointer to a variable that receives the average value.


### -param dStdDev [out]

Pointer to a variable that receives the standard deviation of the values. If the count is less than two, the standard deviation is zero.


### -param dMin [out]

Pointer to a variable that receives the minimum value that was recorded.


### -param dMax [out]

Pointer to a variable that receives the maximum value that was recorded.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

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
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The caller must free the string returned in <i>szName</i>, by calling the <b>SysFreeString</b> function.

To get the number of statistics, call <a href="https://msdn.microsoft.com/48f2543a-7c93-4d4f-a568-b8066e9545fd">IAMStats::get_Count</a>. To get the index of a particular statistic, call <a href="https://msdn.microsoft.com/a5ea650c-42dd-405c-8ad9-6e48cf51353d">IAMStats::GetIndex</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/01dbaba2-fdca-4f42-8816-fd99c4364dbd">IAMStats Interface</a>
 

 

