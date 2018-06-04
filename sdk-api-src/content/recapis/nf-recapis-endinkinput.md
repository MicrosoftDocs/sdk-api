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

# EndInkInput function


## -description



Indicates that no more ink will be added to the context.

You cannot add strokes to the context after calling this function.




## -parameters




### -param hrc

The handle to the recognizer context.


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
The recognizer context handle is invalid or null.

</td>
</tr>
</table>
 




## -remarks



The recognition results you receive after calling this function may be different from previous recognition results that were based on partial ink input.

The Ink Analysis API queries for the implementation of this method. If implemented, the InkAnalyzer will call it each time it performs an analysis operation. If not implemented, EndInkInput is never called. Therefore, you should only expose and implement this method if it is explicitly needed by your recognizer.

<div class="alert"><b>Note</b>  This function is not guaranteed to be called by all applications or operating system components, such as the Tablet PC Input Panel. Therefore, recognizers should not rely on it being called.</div>
<div> </div>


