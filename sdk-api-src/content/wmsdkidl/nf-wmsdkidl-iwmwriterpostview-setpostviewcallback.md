---
UID: NF:wmsdkidl.IWMWriterPostView.SetPostViewCallback
title: IWMWriterPostView::SetPostViewCallback (wmsdkidl.h)
description: The SetPostViewCallback method specifies the callback interface to use for receiving postview samples.
helpviewer_keywords: ["IWMWriterPostView interface [windows Media Format]","SetPostViewCallback method","IWMWriterPostView.SetPostViewCallback","IWMWriterPostView::SetPostViewCallback","IWMWriterPostViewSetPostViewCallback","SetPostViewCallback","SetPostViewCallback method [windows Media Format]","SetPostViewCallback method [windows Media Format]","IWMWriterPostView interface","wmformat.iwmwriterpostview_setpostviewcallback","wmsdkidl/IWMWriterPostView::SetPostViewCallback"]
old-location: wmformat\iwmwriterpostview_setpostviewcallback.htm
tech.root: wmformat
ms.assetid: c2814f32-1787-44a6-8ffc-5d2a9aca8601
ms.date: 12/05/2018
ms.keywords: IWMWriterPostView interface [windows Media Format],SetPostViewCallback method, IWMWriterPostView.SetPostViewCallback, IWMWriterPostView::SetPostViewCallback, IWMWriterPostViewSetPostViewCallback, SetPostViewCallback, SetPostViewCallback method [windows Media Format], SetPostViewCallback method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setpostviewcallback, wmsdkidl/IWMWriterPostView::SetPostViewCallback
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
 - IWMWriterPostView::SetPostViewCallback
 - wmsdkidl/IWMWriterPostView::SetPostViewCallback
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
 - IWMWriterPostView.SetPostViewCallback
---

# IWMWriterPostView::SetPostViewCallback


## -description

The <b>SetPostViewCallback</b> method specifies the callback interface to use for receiving postview samples.

## -parameters

### -param pCallback [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback</a> interface.

### -param pvContext [in]

Generic pointer, for use by the application.

## -returns

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview">IWMWriterPostView Interface</a>