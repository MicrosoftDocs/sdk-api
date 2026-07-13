---
UID: NF:wmsdkidl.IWMSyncReader.Close
title: IWMSyncReader::Close (wmsdkidl.h)
description: The Close method removes a file from the synchronous reader.
helpviewer_keywords: ["Close","Close method [windows Media Format]","Close method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","Close method","IWMSyncReader.Close","IWMSyncReader::Close","IWMSyncReaderClose","wmformat.iwmsyncreader_close","wmsdkidl/IWMSyncReader::Close"]
old-location: wmformat\iwmsyncreader_close.htm
tech.root: wmformat
ms.assetid: 98f5a44f-dc34-4732-b497-5528de6af1c3
ms.date: 4/26/2023
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],Close method, IWMSyncReader.Close, IWMSyncReader::Close, IWMSyncReaderClose, wmformat.iwmsyncreader_close, wmsdkidl/IWMSyncReader::Close
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
 - IWMSyncReader::Close
 - wmsdkidl/IWMSyncReader::Close
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
 - IWMSyncReader.Close
---

# IWMSyncReader::Close


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Close</b> method removes a file from the synchronous reader.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-open">IWMSyncReader::Open</a>
