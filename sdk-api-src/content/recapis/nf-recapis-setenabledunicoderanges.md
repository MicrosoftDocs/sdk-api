---
UID: NF:recapis.SetEnabledUnicodeRanges
title: SetEnabledUnicodeRanges function
author: windows-sdk-content
description: Enables one or more Unicode point ranges on the context.
old-location: tablet\setenabledunicoderanges.htm
old-project: tablet
ms.assetid: 68c7c06b-eab1-419d-ad58-22cbd4c3065e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 68c7c06b-eab1-419d-ad58-22cbd4c3065e, SetEnabledUnicodeRanges, SetEnabledUnicodeRanges function [Tablet PC], recapis/SetEnabledUnicodeRanges, tablet.setenabledunicoderanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: recapis.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
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
 - SetEnabledUnicodeRanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# SetEnabledUnicodeRanges function


## -description



Enables one or more Unicode point ranges on the context.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param cRanges

The number of ranges in the <i>pRanges</i> buffer.


### -param pcr

An array of <a href="https://msdn.microsoft.com/51d13adf-170e-4172-b752-c9dac5a96fa5">CHARACTER_RANGE</a> structures. Each structure identifies a range of Unicode points that you want to enable in the recognizer. The order of the array is arbitrary.


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
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support one of the specified Unicode point ranges.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The <b>SetEnabledUnicodeRanges</b> function is optional.

Some recognizers do not support enabling and disabling specific code points, but may still include the <b>SetEnabledUnicodeRanges</b> function. For such recognizers, the <b>SetEnabledUnicodeRanges</b> function returns E_NOTIMPL.

Each recognizer supports one or more Unicode point ranges. To determine which Unicode point ranges the recognizer supports, call the <a href="https://msdn.microsoft.com/4a354073-e971-43ba-93c9-84fa2e8c59aa">GetUnicodeRanges</a> function. If you do not call this function, the recognizer uses a default set of Unicode point ranges. The default ranges are recognizer specific.

The Microsoft gesture recognizer uses Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="https://msdn.microsoft.com/931fc69a-1f7a-492c-8158-0691cd2fe57a">Unicode Range Values of Gestures</a>.




## -see-also




<a href="https://msdn.microsoft.com/51d13adf-170e-4172-b752-c9dac5a96fa5">CHARACTER_RANGE Structure</a>



<a href="https://msdn.microsoft.com/047a72f9-a627-4c8b-b271-13d3c873abc9">GetEnabledUnicodeRanges Function</a>



<a href="https://msdn.microsoft.com/4a354073-e971-43ba-93c9-84fa2e8c59aa">GetUnicodeRanges Function</a>
 

 

