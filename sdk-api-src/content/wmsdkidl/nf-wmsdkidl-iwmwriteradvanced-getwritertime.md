---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetWriterTime
title: IWMWriterAdvanced::GetWriterTime (wmsdkidl.h)
description: The GetWriterTime method retrieves the clock time that the writer is working to.
helpviewer_keywords: ["GetWriterTime","GetWriterTime method [windows Media Format]","GetWriterTime method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetWriterTime method","IWMWriterAdvanced.GetWriterTime","IWMWriterAdvanced::GetWriterTime","IWMWriterAdvancedGetWriterTime","wmformat.iwmwriteradvanced_getwritertime","wmsdkidl/IWMWriterAdvanced::GetWriterTime"]
old-location: wmformat\iwmwriteradvanced_getwritertime.htm
tech.root: wmformat
ms.assetid: ed15e545-8b37-4098-8e2f-96f4cfb271d3
ms.date: 12/05/2018
ms.keywords: GetWriterTime, GetWriterTime method [windows Media Format], GetWriterTime method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetWriterTime method, IWMWriterAdvanced.GetWriterTime, IWMWriterAdvanced::GetWriterTime, IWMWriterAdvancedGetWriterTime, wmformat.iwmwriteradvanced_getwritertime, wmsdkidl/IWMWriterAdvanced::GetWriterTime
f1_keywords:
- wmsdkidl/IWMWriterAdvanced.GetWriterTime
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
- IWMWriterAdvanced.GetWriterTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced::GetWriterTime


## -description



The <b>GetWriterTime</b> method retrieves the clock time that the writer is working to.




## -parameters




### -param pcnsCurrentTime [out]

Pointer to a variable containing the current time in 100-nanosecond units.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcnsCurrentTime</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method returns the largest time stamp that the writer can currently process. This time stamp will increase as data is produced by the writer. This method can be used to ensure that data is delivered to the writer at the proper rate.

The time returned is the number of 100-nanosecond units since the call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>.

The writer can be running in real time. Call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-isrealtime">IWMWriterAdvanced::IsRealTime</a> method to ascertain whether this is true.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>
 

 

