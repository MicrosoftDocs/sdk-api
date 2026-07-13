---
UID: NF:wmsdkidl.IWMMediaProps.GetMediaType
title: IWMMediaProps::GetMediaType (wmsdkidl.h)
description: The GetMediaType method retrieves a structure describing the media type.
helpviewer_keywords: ["GetMediaType","GetMediaType method [windows Media Format]","GetMediaType method [windows Media Format]","IWMMediaProps interface","IWMMediaProps interface [windows Media Format]","GetMediaType method","IWMMediaProps.GetMediaType","IWMMediaProps::GetMediaType","IWMMediaPropsGetMediaType","wmformat.iwmmediaprops_getmediatype","wmsdkidl/IWMMediaProps::GetMediaType"]
old-location: wmformat\iwmmediaprops_getmediatype.htm
tech.root: wmformat
ms.assetid: 8357e5c6-d8c6-4a30-8446-85fa7fa118f7
ms.date: 4/26/2023
ms.keywords: GetMediaType, GetMediaType method [windows Media Format], GetMediaType method [windows Media Format],IWMMediaProps interface, IWMMediaProps interface [windows Media Format],GetMediaType method, IWMMediaProps.GetMediaType, IWMMediaProps::GetMediaType, IWMMediaPropsGetMediaType, wmformat.iwmmediaprops_getmediatype, wmsdkidl/IWMMediaProps::GetMediaType
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
 - IWMMediaProps::GetMediaType
 - wmsdkidl/IWMMediaProps::GetMediaType
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
 - IWMMediaProps.GetMediaType
---

# IWMMediaProps::GetMediaType


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMediaType</b> method retrieves a structure describing the media type.

## -parameters

### -param pType [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a> structure. If this parameter is set to <b>NULL</b>, this method returns the size of the buffer required in the <i>pcbType</i> parameter.

### -param pcbType [in, out]

On input, the size of the <i>pType</i> buffer. On output, if <i>pType</i> is set to <b>NULL</b>, the value this points to is set to the size of the buffer needed to hold the media type structure.

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
The <i>pcbType</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcbType</i> parameter is not large enough.

</td>
</tr>
</table>

## -remarks

You must make two calls to <b>GetMediaType</b>. On the first call, pass <b>NULL</b> as <i>pType</i>. On return, the value of <i>pcbType</i> will be set to the buffer size required to hold the <b>WM_MEDIA_TYPE</b> structure. Then you can allocate a buffer of the required size and pass a pointer to it as <i>pType</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype">IWMMediaProps::SetMediaType</a>



<a href="/windows/desktop/wmformat/media-types">Media Types</a>