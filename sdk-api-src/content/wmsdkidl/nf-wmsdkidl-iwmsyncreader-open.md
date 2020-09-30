---
UID: NF:wmsdkidl.IWMSyncReader.Open
title: IWMSyncReader::Open (wmsdkidl.h)
description: The Open method opens a file for reading. Unlike IWMReader::Open, this method is a synchronous call.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","Open method","IWMSyncReader.Open","IWMSyncReader::Open","IWMSyncReaderOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_open","wmsdkidl/IWMSyncReader::Open"]
old-location: wmformat\iwmsyncreader_open.htm
tech.root: wmformat
ms.assetid: dab1a9c4-487c-4b20-909e-05f3504698f5
ms.date: 12/05/2018
ms.keywords: IWMSyncReader interface [windows Media Format],Open method, IWMSyncReader.Open, IWMSyncReader::Open, IWMSyncReaderOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_open, wmsdkidl/IWMSyncReader::Open
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
 - IWMSyncReader::Open
 - wmsdkidl/IWMSyncReader::Open
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
 - IWMSyncReader.Open
---

# IWMSyncReader::Open


## -description

The <b>Open</b> method opens a file for reading. Unlike <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>, this method is a synchronous call.

## -parameters

### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name to open. This must be a valid file name with an ASF file extension or an MP3 file name.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The synchronous reader does not support streaming media. Passing a URL as <i>pwszFilename</i> results in an error.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-close">IWMSyncReader::Close</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream">IWMSyncReader::OpenStream</a>