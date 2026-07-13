---
UID: NF:wmsdkidl.IWMWriterFileSink3.SetUnbufferedIO
title: IWMWriterFileSink3::SetUnbufferedIO (wmsdkidl.h)
description: The SetUnbufferedIO method specifies whether unbuffered I/O is used for the file sink. You can improve performance by using unbuffered I/O for writer sessions with a high bit rate and a long running time.
helpviewer_keywords: ["IWMWriterFileSink3 interface [windows Media Format]","SetUnbufferedIO method","IWMWriterFileSink3.SetUnbufferedIO","IWMWriterFileSink3::SetUnbufferedIO","IWMWriterFileSink3SetUnbufferedIO","SetUnbufferedIO","SetUnbufferedIO method [windows Media Format]","SetUnbufferedIO method [windows Media Format]","IWMWriterFileSink3 interface","wmformat.iwmwriterfilesink3_setunbufferedio","wmsdkidl/IWMWriterFileSink3::SetUnbufferedIO"]
old-location: wmformat\iwmwriterfilesink3_setunbufferedio.htm
tech.root: wmformat
ms.assetid: 51a9c21b-d301-41e4-a9bc-321a5b2decca
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink3 interface [windows Media Format],SetUnbufferedIO method, IWMWriterFileSink3.SetUnbufferedIO, IWMWriterFileSink3::SetUnbufferedIO, IWMWriterFileSink3SetUnbufferedIO, SetUnbufferedIO, SetUnbufferedIO method [windows Media Format], SetUnbufferedIO method [windows Media Format],IWMWriterFileSink3 interface, wmformat.iwmwriterfilesink3_setunbufferedio, wmsdkidl/IWMWriterFileSink3::SetUnbufferedIO
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMWriterFileSink3::SetUnbufferedIO
 - wmsdkidl/IWMWriterFileSink3::SetUnbufferedIO
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
 - IWMWriterFileSink3.SetUnbufferedIO
---

# IWMWriterFileSink3::SetUnbufferedIO


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetUnbufferedIO</b> method specifies whether unbuffered I/O is used for the file sink. You can improve performance by using unbuffered I/O for writer sessions with a high bit rate and a long running time.

## -parameters

### -param fUnbufferedIO [in]

A <b>BOOL</b> that specifies whether to use unbuffered I/O.

### -param fRestrictMemUsage [in]

A <b>BOOL</b> that specifies whether memory usage should be restricted. Passing True for this parameter severely limits the size of the buffers used to prepare data for unbuffered writing. This limitation usually counteracts any performance gains from using unbuffered I/O.

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
The header has already been written.

</td>
</tr>
</table>

## -remarks

This method enables the application to override the writer's decision about whether to use unbuffered I/O.

If you want to use unbuffered I/O, you must call this method before writing the header of the file.

This method dynamically allocates a set of buffers to prepare data for unbuffered writing. The size of these buffers is dependent upon the amount of available physical memory.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getunbufferedio">IWMWriterFileSink3::GetUnbufferedIO</a>