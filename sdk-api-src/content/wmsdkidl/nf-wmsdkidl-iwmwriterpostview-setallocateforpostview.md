---
UID: NF:wmsdkidl.IWMWriterPostView.SetAllocateForPostView
title: IWMWriterPostView::SetAllocateForPostView (wmsdkidl.h)
description: The SetAllocateForPostView method specifies whether the application, and not the writer, must supply the buffers.
helpviewer_keywords: ["IWMWriterPostView interface [windows Media Format]","SetAllocateForPostView method","IWMWriterPostView.SetAllocateForPostView","IWMWriterPostView::SetAllocateForPostView","IWMWriterPostViewSetAllocateForPostView","SetAllocateForPostView","SetAllocateForPostView method [windows Media Format]","SetAllocateForPostView method [windows Media Format]","IWMWriterPostView interface","wmformat.iwmwriterpostview_setallocateforpostview","wmsdkidl/IWMWriterPostView::SetAllocateForPostView"]
old-location: wmformat\iwmwriterpostview_setallocateforpostview.htm
tech.root: wmformat
ms.assetid: 995bf3fa-3e10-46a2-ad51-55375d6af447
ms.date: 4/26/2023
ms.keywords: IWMWriterPostView interface [windows Media Format],SetAllocateForPostView method, IWMWriterPostView.SetAllocateForPostView, IWMWriterPostView::SetAllocateForPostView, IWMWriterPostViewSetAllocateForPostView, SetAllocateForPostView, SetAllocateForPostView method [windows Media Format], SetAllocateForPostView method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setallocateforpostview, wmsdkidl/IWMWriterPostView::SetAllocateForPostView
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
 - IWMWriterPostView::SetAllocateForPostView
 - wmsdkidl/IWMWriterPostView::SetAllocateForPostView
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
 - IWMWriterPostView.SetAllocateForPostView
---

# IWMWriterPostView::SetAllocateForPostView


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAllocateForPostView</b> method specifies whether the application, and not the writer, must supply the buffers.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param fAllocate [in]

Boolean value. Set to True if the application allocates buffers, and False if this is left to the reader.

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
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The stream number specified by <i>wStreamNumber</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to create an internal structure.

</td>
</tr>
</table>

## -remarks

The application can provide buffers for any of the outputs, rather than use those allocated by the reader. For example, some applications can allocate Microsoft DirectDraw® buffers.

The actual allocation of buffers is handled by the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a> interface.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getallocateforpostview">IWMWriterPostView::GetAllocateForPostView</a>