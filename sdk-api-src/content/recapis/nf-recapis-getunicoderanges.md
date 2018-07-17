---
UID: NF:recapis.GetUnicodeRanges
title: GetUnicodeRanges function
author: windows-sdk-content
description: Returns the ranges of Unicode points that the recognizer supports.
old-location: tablet\getunicoderanges.htm
old-project: tablet
ms.assetid: 4a354073-e971-43ba-93c9-84fa2e8c59aa
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 4a354073-e971-43ba-93c9-84fa2e8c59aa, GetUnicodeRanges, GetUnicodeRanges function [Tablet PC], recapis/GetUnicodeRanges, tablet.getunicoderanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetUnicodeRanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# GetUnicodeRanges function


## -description



Returns the ranges of Unicode points that the recognizer supports.




## -parameters




### -param hrec

Handle to the recognizer.


### -param pcRanges

On input, the number of ranges the <i>pcr</i> buffer can hold. On output, the number of ranges the <i>pcr</i> buffer contains.


### -param pcr

Array of <a href="https://msdn.microsoft.com/51d13adf-170e-4172-b752-c9dac5a96fa5">CHARACTER_RANGE</a> structures. Each structure contains a range of Unicode points that the recognizer supports. The order of the array is arbitrary. To determine the required size of the buffer, set <i>pcr</i> to <b>NULL</b>; use the number of ranges to allocate the <i>pcr</i> buffer.


## -returns



This function can return one of these values.

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
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcr</i> buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

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
</table>
 




## -remarks



This function is optional.

Some recognizers do not support this capability, but may still include the <b>GetUnicodeRanges Function</b> function. For such recognizers the <b>GetUnicodeRanges</b> function returns E_NOTIMPL.

To control the Unicode ranges used by a specific recognizer context, use the <a href="https://msdn.microsoft.com/047a72f9-a627-4c8b-b271-13d3c873abc9">GetEnabledUnicodeRanges</a> and <a href="https://msdn.microsoft.com/68c7c06b-eab1-419d-ad58-22cbd4c3065e">SetEnabledUnicodeRanges</a> functions. These ranges are constrained to be a subset of the ranges returned by <b>GetUnicodeRanges</b>.


          Microsoft gesture recognizers use Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="https://msdn.microsoft.com/931fc69a-1f7a-492c-8158-0691cd2fe57a">Unicode Range Values of Gestures</a>.




## -see-also




<a href="https://msdn.microsoft.com/047a72f9-a627-4c8b-b271-13d3c873abc9">GetEnabledUnicodeRanges Function</a>



<a href="https://msdn.microsoft.com/68c7c06b-eab1-419d-ad58-22cbd4c3065e">SetEnabledUnicodeRanges Function</a>
 

 

