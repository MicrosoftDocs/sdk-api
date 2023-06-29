---
UID: NF:wmsdkidl.IWMMediaProps.GetType
title: IWMMediaProps::GetType (wmsdkidl.h)
description: The GetType method retrieves the major type of the media in the stream, input, or output described by the object to which the current IWMMediaProps interface belongs.
helpviewer_keywords: ["GetType","GetType method [windows Media Format]","GetType method [windows Media Format]","IWMMediaProps interface","IWMMediaProps interface [windows Media Format]","GetType method","IWMMediaProps.GetType","IWMMediaProps::GetType","IWMMediaPropsGetType","wmformat.iwmmediaprops_gettype","wmsdkidl/IWMMediaProps::GetType"]
old-location: wmformat\iwmmediaprops_gettype.htm
tech.root: wmformat
ms.assetid: d878caf9-2cd2-4b1d-b204-a43fe947c4c2
ms.date: 4/26/2023
ms.keywords: GetType, GetType method [windows Media Format], GetType method [windows Media Format],IWMMediaProps interface, IWMMediaProps interface [windows Media Format],GetType method, IWMMediaProps.GetType, IWMMediaProps::GetType, IWMMediaPropsGetType, wmformat.iwmmediaprops_gettype, wmsdkidl/IWMMediaProps::GetType
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
 - IWMMediaProps::GetType
 - wmsdkidl/IWMMediaProps::GetType
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
 - IWMMediaProps.GetType
---

# IWMMediaProps::GetType


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetType</b> method retrieves the major type of the media in the stream, input, or output described by the object to which the current <b>IWMMediaProps</b> interface belongs.

## -parameters

### -param pguidType [out]

Pointer to a GUID specifying the media type.

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
The <i>pguidType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

These media types are used by the writer, reader, and profile objects to identify the properties of a media stream that are specific to the media type.

<b>GetType</b> is provided for convenience; it returns the same value as the <b>majortype</b> member of <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype">IWMMediaProps::GetMediaType</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>



<a href="/windows/desktop/wmformat/media-types">Media Types</a>