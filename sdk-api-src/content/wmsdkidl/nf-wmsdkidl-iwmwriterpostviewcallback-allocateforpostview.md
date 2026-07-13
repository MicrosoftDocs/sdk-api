---
UID: NF:wmsdkidl.IWMWriterPostViewCallback.AllocateForPostView
title: IWMWriterPostViewCallback::AllocateForPostView (wmsdkidl.h)
description: The AllocateForPostView method allocates a buffer for use in postviewing operations. The application implements this method.
helpviewer_keywords: ["AllocateForPostView","AllocateForPostView method [windows Media Format]","AllocateForPostView method [windows Media Format]","IWMWriterPostViewCallback interface","IWMWriterPostViewCallback interface [windows Media Format]","AllocateForPostView method","IWMWriterPostViewCallback.AllocateForPostView","IWMWriterPostViewCallback::AllocateForPostView","IWMWriterPostViewCallbackAllocateForPostView","wmformat.iwmwriterpostviewcallback_allocateforpostview","wmsdkidl/IWMWriterPostViewCallback::AllocateForPostView"]
old-location: wmformat\iwmwriterpostviewcallback_allocateforpostview.htm
tech.root: wmformat
ms.assetid: e48132c4-b222-4401-99b3-7906c0df4ec1
ms.date: 4/26/2023
ms.keywords: AllocateForPostView, AllocateForPostView method [windows Media Format], AllocateForPostView method [windows Media Format],IWMWriterPostViewCallback interface, IWMWriterPostViewCallback interface [windows Media Format],AllocateForPostView method, IWMWriterPostViewCallback.AllocateForPostView, IWMWriterPostViewCallback::AllocateForPostView, IWMWriterPostViewCallbackAllocateForPostView, wmformat.iwmwriterpostviewcallback_allocateforpostview, wmsdkidl/IWMWriterPostViewCallback::AllocateForPostView
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterPostViewCallback::AllocateForPostView
 - wmsdkidl/IWMWriterPostViewCallback::AllocateForPostView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMWriterPostViewCallback.AllocateForPostView
---

# IWMWriterPostViewCallback::AllocateForPostView


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AllocateForPostView</b> method allocates a buffer for use in postviewing operations. The application implements this method.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.

### -param ppBuffer [out]

Pointer to a pointer to an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface.

### -param pvContext [in]

Generic pointer, for use by the application.

## -returns

This method is implemented by the application. It should return S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback Interface</a>