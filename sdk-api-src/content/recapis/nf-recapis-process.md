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

# Process function


## -description



Performs ink recognition synchronously.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pbPartialProcessing

Specify <b>TRUE</b> to process a subset of the ink. Partial processing reduces the time the recognizer spends performing recognition if more ink is expected.

Typically an application specifies <b>FALSE</b> to process all the ink. The function does not process all the ink if you have not called the <a href="https://msdn.microsoft.com/a384edf8-3b3d-4e0c-b39c-976798457076">EndInkInput</a> function.

The function sets the <i>pbPartialProcessing</i> parameter to <b>TRUE</b> if there is enough ink left to continue processing; otherwise, <b>FALSE</b>.


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
The function did not process the ink because the ink has been fully processed, or the <a href="https://msdn.microsoft.com/a384edf8-3b3d-4e0c-b39c-976798457076">EndInkInput</a> function has not been called and the recognizer does not support incremental processing of ink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_S_INTERRUPTED</b></dt>
</dl>
</td>
<td width="60%">
The process was interrupted by a call to the <a href="https://msdn.microsoft.com/326bbbff-4adc-46ae-aab3-626b55fecf0c">AdviseInkChange</a> function.

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
</table>
 



