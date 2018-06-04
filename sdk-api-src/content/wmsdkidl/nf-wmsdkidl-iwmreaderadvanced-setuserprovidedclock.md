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

# IWMReaderAdvanced::SetUserProvidedClock


## -description



The <b>SetUserProvidedClock</b> method specifies whether a clock provided by the application is to be used.




## -parameters




### -param fUserClock [in]

Boolean value that is True if an application-provided clock is to be used.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The reader is not properly configured to handle this request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to set an internal event.

</td>
</tr>
</table>
 




## -remarks



In some cases, an application built on this SDK requires the clock to be driven by the application rather than by real time. This is true, for example, if the application reads from a file at a rate faster than it takes to play the file. User-provided clocks are only supported when the source file is a local file.

This method can fail if the current source does not support user-provided clocks. To drive a clock, an application must call <a href="https://msdn.microsoft.com/5e47ef96-9971-47b0-a003-b38f4045da7a">DeliverTime</a>, and then wait for <a href="https://msdn.microsoft.com/9913bbc4-df59-484f-b050-324e2ecdeb1c">IWMReaderCallbackAdvanced::OnTime</a> to reach the time specified.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/54eb30ae-4b84-489c-a5e5-e73dee2c5056">IWMReaderAdvanced::GetUserProvidedClock</a>
 

 

