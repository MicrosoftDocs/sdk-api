---
UID: NF:recapis.GetGuide
title: GetGuide function
author: windows-sdk-content
description: Retrieves the guide used for boxed, lined, or freeform input.
old-location: tablet\getguide.htm
tech.root: tablet
ms.assetid: b86d6266-cce3-4f84-80b6-7d136172b3ca
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetGuide, GetGuide function [Tablet PC], b86d6266-cce3-4f84-80b6-7d136172b3ca, recapis/GetGuide, tablet.getguide
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetGuide
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetGuide function


## -description



Retrieves the guide used for boxed, lined, or freeform input.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pGuide

A guide used for boxed, lined, or freeform input. For guide details, see the <a href="https://msdn.microsoft.com/e28347aa-08ed-4f40-b9c3-4d3b5dacbeb7">RECO_GUIDE</a> structure.


### -param piIndex

Index value of the first box or line in the context.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The context does not contain a guide.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e28347aa-08ed-4f40-b9c3-4d3b5dacbeb7">RECO_GUIDE Structure</a>



<a href="https://msdn.microsoft.com/3ca3c743-83f9-46b0-851a-cba6e4ed980a">SetGuide Function</a>
 

 

