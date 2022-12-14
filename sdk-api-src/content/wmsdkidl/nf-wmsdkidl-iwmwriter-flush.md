---
UID: NF:wmsdkidl.IWMWriter.Flush
title: IWMWriter::Flush (wmsdkidl.h)
description: The functionality of the Flush method has been removed, because IWMWriter::EndWriting performs the needed checks internally. For compatibility with older applications, calls to flush will always return S_OK even though the call does nothing.
helpviewer_keywords: ["Flush","Flush method [windows Media Format]","Flush method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","Flush method","IWMWriter.Flush","IWMWriter::Flush","IWMWriterFlush","wmformat.iwmwriter_flush","wmsdkidl/IWMWriter::Flush"]
old-location: wmformat\iwmwriter_flush.htm
tech.root: wmformat
ms.assetid: 1fa0c482-f1f5-4d3c-8268-731914caefa3
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [windows Media Format], Flush method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],Flush method, IWMWriter.Flush, IWMWriter::Flush, IWMWriterFlush, wmformat.iwmwriter_flush, wmsdkidl/IWMWriter::Flush
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
 - IWMWriter::Flush
 - wmsdkidl/IWMWriter::Flush
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
 - IWMWriter.Flush
---

# IWMWriter::Flush


## -description

The functionality of the <b>Flush</b> method has been removed, because <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting">IWMWriter::EndWriting</a> performs the needed checks internally. For compatibility with older applications, calls to flush will always return S_OK even though the call does nothing.



## -returns

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>
