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

# IInterval::GetLimits


## -description


Specifies the lower and upper limits of an interval, each of which may be infinite or a specific value.
        


When a condition tree expresses that the value of a property must fall in a certain range, the property can be expressed as a leaf node. The node must be a <a href="_stg_propvariant">PROPVARIANT</a> containing a <b>vt</b> value type tag of VT_UNKNOWN and an IUnknown* <b>punkVal</b> that is a pointer to an object that implements <a href="https://msdn.microsoft.com/b8a55ff7-cbe0-4f58-ad93-1a26ecf3fd7c">IInterval</a>.


## -parameters




### -param pilkLower [out]

Type: <b><a href="https://msdn.microsoft.com/02b25f59-d00f-4ffa-bb7c-f02089235f4f">INTERVAL_LIMIT_KIND</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/02b25f59-d00f-4ffa-bb7c-f02089235f4f">INTERVAL_LIMIT_KIND</a> enumeration that indicates whether the lower bound of the interval is inclusive, exclusive, or infinite.


### -param ppropvarLower [out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

Receives a pointer to the value for the lower limit of the interval. If the <i>pilkLower</i> parameter is set to <i>ILK_NEGATIVE_INFINITY</i> or <i>ILK_POSITIVE_INFINITY</i>, this value is set to <b>VT_EMPTY</b>.


### -param pilkUpper [out]

Type: <b><a href="https://msdn.microsoft.com/02b25f59-d00f-4ffa-bb7c-f02089235f4f">INTERVAL_LIMIT_KIND</a>*</b>

Receives a pointer to a value from the <a href="https://msdn.microsoft.com/02b25f59-d00f-4ffa-bb7c-f02089235f4f">INTERVAL_LIMIT_KIND</a> enumeration that indicates whether the upper bound of the interval is inclusive, exclusive, or infinite. 


### -param ppropvarUpper [out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

Receives a pointer to the value for the upper limit of the interval. If the <i>pilkUpper</i> parameter is set to <i>ILK_NEGATIVE_INFINITY</i> or <i>ILK_POSITIVE_INFINITY</i>, this value will be set to <b>VT_EMPTY</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves interval limits in two <a href="https://msdn.microsoft.com/02b25f59-d00f-4ffa-bb7c-f02089235f4f">INTERVAL_LIMIT_KIND</a>—<a href="_stg_propvariant">PROPVARIANT</a> pairs. The first pair specifies the lower limit of the interval, and the second pari specifies the upper limit of the interval. 

The lower limit must be less than the upper limit or the interval will be empty. The only exception is when the lower and upper limits are equal and both are set to <i>ILK_EXPLICIT_INCLUDED</i>. In this case the range is the single value to which both limits are set. The following table illustrates how the pairs work to define intervals.



<table class="clsStd">
<tr>
<th>pilkLower</th>
<th>ppropvarLower</th>
<th>pilkLower</th>
<th>ppropvarLower</th>
<th>Description</th>
</tr>
<tr>
<td>ILK_EXPLICIT_INCLUDED</td>
<td>3</td>
<td>ILK_EXPLICIT_INCLUDED</td>
<td>3</td>
<td>
The lowest value in the range is 3 because the 3 is explicitly included in the range.

The highest value in the range is also 3 (explicitly included), and the interval consists of only the number 3.

</td>
</tr>
<tr>
<td>ILK_EXPLICIT_INCLUDED</td>
<td>3</td>
<td>ILK_EXPLICIT_EXCLUDED</td>
<td>3</td>
<td>The lowest value in the range is 3 (explicitly included), but the upper limit is also 3 and is explicitly excluded. Therefore, the interval being described is an empty interval.</td>
</tr>
<tr>
<td>ILK_EXPLICIT_INCLUDED</td>
<td>3</td>
<td>ILK_EXPLICIT_EXCLUDED</td>
<td>6</td>
<td>The integer interval begins at and includes 3, and ends at but does not include 6.</td>
</tr>
<tr>
<td>ILK_NEGATIVE_INFINITY</td>
<td>VT_EMPTY</td>
<td>ILK_POSITIVE_INFINITY</td>
<td>VT_EMPTY</td>
<td>All integers are included in the interval.</td>
</tr>
</table>
 



