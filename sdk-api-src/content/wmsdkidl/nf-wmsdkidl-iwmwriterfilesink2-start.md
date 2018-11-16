---
UID: NF:wmsdkidl.IWMWriterFileSink2.Start
title: IWMWriterFileSink2::Start
author: windows-sdk-content
description: The Start method starts recording at the specified time.
old-location: wmformat\iwmwriterfilesink2_start.htm
tech.root: wmformat
ms.assetid: b4bfddbb-9156-42bf-b8d5-424fff9f4b64
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],Start method, IWMWriterFileSink2.Start, IWMWriterFileSink2::Start, IWMWriterFileSink2Start, Start, Start method [windows Media Format], Start method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_start, wmsdkidl/IWMWriterFileSink2::Start
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterFileSink2.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMWriterFileSink2.Start
: 
---

# IWMWriterFileSink2::Start


## -description



The <b>Start</b> method starts recording at the specified time.




## -parameters




### -param cnsStartTime [in]

Start time in 100-nanosecond units.


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
The requested start time precedes the last stop time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete the task.

</td>
</tr>
</table>
 




## -remarks



It is not necessary to call this method unless the sink has been stopped. The sink automatically starts (at time 0) when it is added to the writer by using <a href="https://msdn.microsoft.com/65763ac3-fba0-4de6-9c2e-4e241bbe5f13">IWMWriterAdvanced::AddSink</a>.

Because of interleaving of streams with slightly different time stamps at any particular point in the file, the actual start time might not be exactly as specified in <i>cnsStartTime</i>. To increase the precision, call <a href="https://msdn.microsoft.com/c103d205-a568-4206-a66e-5473e16cfa3f">IWMWriterFileSink3::SetControlStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>



<a href="https://msdn.microsoft.com/8d1bce07-a165-45cf-95cb-03b57f0cae03">IWMWriterFileSink2::Close</a>



<a href="https://msdn.microsoft.com/47377c77-f534-4bb0-be57-49bdb109c309">IWMWriterFileSink2::Stop</a>
 

 

