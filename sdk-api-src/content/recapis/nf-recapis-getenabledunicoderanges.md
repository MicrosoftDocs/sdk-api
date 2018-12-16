---
UID: NF:recapis.GetEnabledUnicodeRanges
title: GetEnabledUnicodeRanges function
author: windows-sdk-content
description: Retrieves a list of Unicode point ranges enabled on the context. If you do not call the SetEnabledUnicodeRanges function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges.
old-location: tablet\getenabledunicoderanges.htm
tech.root: tablet
ms.assetid: 047a72f9-a627-4c8b-b271-13d3c873abc9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 047a72f9-a627-4c8b-b271-13d3c873abc9, GetEnabledUnicodeRanges, GetEnabledUnicodeRanges function [Tablet PC], recapis/GetEnabledUnicodeRanges, tablet.getenabledunicoderanges
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetEnabledUnicodeRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetEnabledUnicodeRanges function


## -description



Retrieves a list of Unicode point ranges enabled on the context. If you do not call the <a href="https://msdn.microsoft.com/68c7c06b-eab1-419d-ad58-22cbd4c3065e">SetEnabledUnicodeRanges</a> function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pcRanges

On input, the number of <a href="https://msdn.microsoft.com/51d13adf-170e-4172-b752-c9dac5a96fa5">CHARACTER_RANGE</a> structures the <i>pcr</i> buffer can contain. On output, the number of ranges the <i>pcr</i> buffer contains.


### -param pcr

An array of CHARACTER_RANGE structures. Each structure contains a range of Unicode points enabled on the context. The order of the array is arbitrary. To determine the size of the buffer, set <i>pcr</i> to <b>NULL</b>; use the number of ranges to allocate the <i>pcr</i> buffer.


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

Some recognizers do not support enabling and disabling specific Unicode points, but may still include the <b>GetEnabledUnicodeRanges</b> function. For such recognizers the <b>GetEnabledUnicodeRanges</b> function returns the same ranges as the <a href="https://msdn.microsoft.com/4a354073-e971-43ba-93c9-84fa2e8c59aa">GetUnicodeRanges</a> function.

Microsoft gesture recognizers use Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="https://msdn.microsoft.com/931fc69a-1f7a-492c-8158-0691cd2fe57a">Unicode Range Values of Gestures</a>.




## -see-also




<a href="https://msdn.microsoft.com/51d13adf-170e-4172-b752-c9dac5a96fa5">CHARACTER_RANGE Structure</a>



<a href="https://msdn.microsoft.com/4a354073-e971-43ba-93c9-84fa2e8c59aa">GetUnicodeRanges Function</a>



<a href="https://msdn.microsoft.com/68c7c06b-eab1-419d-ad58-22cbd4c3065e">SetEnabledUnicodeRanges Function</a>
 

 

