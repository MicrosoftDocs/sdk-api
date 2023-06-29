---
UID: NF:wmsdkidl.IWMReaderAccelerator.Notify
title: IWMReaderAccelerator::Notify (wmsdkidl.h)
description: The Notify method is called by the source filter to pass in the negotiated media type.
helpviewer_keywords: ["IWMReaderAccelerator interface [windows Media Format]","Notify method","IWMReaderAccelerator.Notify","IWMReaderAccelerator::Notify","IWMReaderAcceleratorNotify","Notify","Notify method [windows Media Format]","Notify method [windows Media Format]","IWMReaderAccelerator interface","wmformat.iwmreaderaccelerator_notify","wmsdkidl/IWMReaderAccelerator::Notify"]
old-location: wmformat\iwmreaderaccelerator_notify.htm
tech.root: wmformat
ms.assetid: b5381f3a-e120-4db3-8463-5286e4318b13
ms.date: 4/26/2023
ms.keywords: IWMReaderAccelerator interface [windows Media Format],Notify method, IWMReaderAccelerator.Notify, IWMReaderAccelerator::Notify, IWMReaderAcceleratorNotify, Notify, Notify method [windows Media Format], Notify method [windows Media Format],IWMReaderAccelerator interface, wmformat.iwmreaderaccelerator_notify, wmsdkidl/IWMReaderAccelerator::Notify
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
 - IWMReaderAccelerator::Notify
 - wmsdkidl/IWMReaderAccelerator::Notify
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
 - IWMReaderAccelerator.Notify
---

# IWMReaderAccelerator::Notify


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Notify</b> method is called by the source filter to pass in the negotiated media type.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> that specifies the stream associated with the notification.

### -param pSubtype [in]

Pointer to a media type that describes the current connection parameters for the stream.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .

## -remarks

This method enables the reader to update its internal variables and commit to the DirectX VA connection. This is the last place the decoder or reader can fail.

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator">IWMReaderAccelerator Interface</a>