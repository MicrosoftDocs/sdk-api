---
UID: NF:wmsdkidl.IWMWriterPushSink.Disconnect
title: IWMWriterPushSink::Disconnect (wmsdkidl.h)
description: The Disconnect method disconnects the push sink from the server.
helpviewer_keywords: ["Disconnect","Disconnect method [windows Media Format]","Disconnect method [windows Media Format]","IWMWriterPushSink interface","IWMWriterPushSink interface [windows Media Format]","Disconnect method","IWMWriterPushSink.Disconnect","IWMWriterPushSink::Disconnect","IWMWriterPushSinkDisconnect","wmformat.iwmwriterpushsink_disconnect","wmsdkidl/IWMWriterPushSink::Disconnect"]
old-location: wmformat\iwmwriterpushsink_disconnect.htm
tech.root: wmformat
ms.assetid: 37e8badb-139a-45bf-84bc-bb071d128847
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [windows Media Format], Disconnect method [windows Media Format],IWMWriterPushSink interface, IWMWriterPushSink interface [windows Media Format],Disconnect method, IWMWriterPushSink.Disconnect, IWMWriterPushSink::Disconnect, IWMWriterPushSinkDisconnect, wmformat.iwmwriterpushsink_disconnect, wmsdkidl/IWMWriterPushSink::Disconnect
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
 - IWMWriterPushSink::Disconnect
 - wmsdkidl/IWMWriterPushSink::Disconnect
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
 - IWMWriterPushSink.Disconnect
---

# IWMWriterPushSink::Disconnect


## -description

The <b>Disconnect</b> method disconnects the push sink from the server.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The data path on the downstream server remains active for 5 minutes, after which it is cleaned up.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink">IWMWriterPushSink Interface</a>
