---
UID: NF:wmsdkidl.IWMIndexer.Cancel
title: IWMIndexer::Cancel (wmsdkidl.h)
description: The Cancel method cancels the current indexing operation.
helpviewer_keywords: ["Cancel","Cancel method [windows Media Format]","Cancel method [windows Media Format]","IWMIndexer interface","IWMIndexer interface [windows Media Format]","Cancel method","IWMIndexer.Cancel","IWMIndexer::Cancel","IWMIndexerCancel","wmformat.iwmindexer_cancel","wmsdkidl/IWMIndexer::Cancel"]
old-location: wmformat\iwmindexer_cancel.htm
tech.root: wmformat
ms.assetid: 8f6061bc-fb11-484a-b5b2-f56827e0fea9
ms.date: 4/26/2023
ms.keywords: Cancel, Cancel method [windows Media Format], Cancel method [windows Media Format],IWMIndexer interface, IWMIndexer interface [windows Media Format],Cancel method, IWMIndexer.Cancel, IWMIndexer::Cancel, IWMIndexerCancel, wmformat.iwmindexer_cancel, wmsdkidl/IWMIndexer::Cancel
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
 - IWMIndexer::Cancel
 - wmsdkidl/IWMIndexer::Cancel
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
 - IWMIndexer.Cancel
---

# IWMIndexer::Cancel


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Cancel</b> method cancels the current indexing operation.



## -returns

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer Interface</a>
