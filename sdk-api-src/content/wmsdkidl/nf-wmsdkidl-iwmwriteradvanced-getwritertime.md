---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetWriterTime
title: IWMWriterAdvanced::GetWriterTime (wmsdkidl.h)
description: The GetWriterTime method retrieves the clock time that the writer is working to.
helpviewer_keywords: ["GetWriterTime","GetWriterTime method [windows Media Format]","GetWriterTime method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetWriterTime method","IWMWriterAdvanced.GetWriterTime","IWMWriterAdvanced::GetWriterTime","IWMWriterAdvancedGetWriterTime","wmformat.iwmwriteradvanced_getwritertime","wmsdkidl/IWMWriterAdvanced::GetWriterTime"]
old-location: wmformat\iwmwriteradvanced_getwritertime.htm
tech.root: wmformat
ms.assetid: ed15e545-8b37-4098-8e2f-96f4cfb271d3
ms.date: 4/26/2023
ms.keywords: GetWriterTime, GetWriterTime method [windows Media Format], GetWriterTime method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetWriterTime method, IWMWriterAdvanced.GetWriterTime, IWMWriterAdvanced::GetWriterTime, IWMWriterAdvancedGetWriterTime, wmformat.iwmwriteradvanced_getwritertime, wmsdkidl/IWMWriterAdvanced::GetWriterTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterAdvanced::GetWriterTime
 - wmsdkidl/IWMWriterAdvanced::GetWriterTime
dev_langs:
 - c++
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
---

# IWMWriterAdvanced::GetWriterTime


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

The time returned is the number of 100-nanosecond units since the call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>.

The writer can be running in real time. Call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-isrealtime">IWMWriterAdvanced::IsRealTime</a> method to ascertain whether this is true.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>