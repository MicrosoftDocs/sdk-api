---
UID: NF:wmsdkidl.IWMSyncReader.OpenStream
title: IWMSyncReader::OpenStream (wmsdkidl.h)
description: The OpenStream method opens a stream for reading.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","OpenStream method","IWMSyncReader.OpenStream","IWMSyncReader::OpenStream","IWMSyncReaderOpenStream","OpenStream","OpenStream method [windows Media Format]","OpenStream method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_openstream","wmsdkidl/IWMSyncReader::OpenStream"]
old-location: wmformat\iwmsyncreader_openstream.htm
tech.root: wmformat
ms.assetid: ef42495a-2565-4925-882e-c3c42f9d418b
ms.date: 12/05/2018
ms.keywords: IWMSyncReader interface [windows Media Format],OpenStream method, IWMSyncReader.OpenStream, IWMSyncReader::OpenStream, IWMSyncReaderOpenStream, OpenStream, OpenStream method [windows Media Format], OpenStream method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_openstream, wmsdkidl/IWMSyncReader::OpenStream
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
 - IWMSyncReader::OpenStream
 - wmsdkidl/IWMSyncReader::OpenStream
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
 - IWMSyncReader.OpenStream
---

# IWMSyncReader::OpenStream


## -description

The <b>OpenStream</b> method opens a stream for reading.

## -parameters

### -param pStream [in]

Pointer to an <b>IStream</b> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-open">IWMSyncReader::Open</a>