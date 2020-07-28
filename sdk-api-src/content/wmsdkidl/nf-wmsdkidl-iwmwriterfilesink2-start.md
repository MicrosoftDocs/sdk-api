---
UID: NF:wmsdkidl.IWMWriterFileSink2.Start
title: IWMWriterFileSink2::Start (wmsdkidl.h)
description: The Start method starts recording at the specified time.
helpviewer_keywords: ["IWMWriterFileSink2 interface [windows Media Format]","Start method","IWMWriterFileSink2.Start","IWMWriterFileSink2::Start","IWMWriterFileSink2Start","Start","Start method [windows Media Format]","Start method [windows Media Format]","IWMWriterFileSink2 interface","wmformat.iwmwriterfilesink2_start","wmsdkidl/IWMWriterFileSink2::Start"]
old-location: wmformat\iwmwriterfilesink2_start.htm
tech.root: wmformat
ms.assetid: b4bfddbb-9156-42bf-b8d5-424fff9f4b64
ms.date: 12/05/2018
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],Start method, IWMWriterFileSink2.Start, IWMWriterFileSink2::Start, IWMWriterFileSink2Start, Start, Start method [windows Media Format], Start method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_start, wmsdkidl/IWMWriterFileSink2::Start
f1_keywords:
- wmsdkidl/IWMWriterFileSink2.Start
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



It is not necessary to call this method unless the sink has been stopped. The sink automatically starts (at time 0) when it is added to the writer by using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink">IWMWriterAdvanced::AddSink</a>.

Because of interleaving of streams with slightly different time stamps at any particular point in the file, the actual start time might not be exactly as specified in <i>cnsStartTime</i>. To increase the precision, call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setcontrolstream">IWMWriterFileSink3::SetControlStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close">IWMWriterFileSink2::Close</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop">IWMWriterFileSink2::Stop</a>
 

 

