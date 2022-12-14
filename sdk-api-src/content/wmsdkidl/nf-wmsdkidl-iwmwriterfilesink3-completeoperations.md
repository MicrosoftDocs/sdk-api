---
UID: NF:wmsdkidl.IWMWriterFileSink3.CompleteOperations
title: IWMWriterFileSink3::CompleteOperations (wmsdkidl.h)
description: The CompleteOperations method stops the writer sink after completing all operations in progress. This method is used with unbuffered I/O.
helpviewer_keywords: ["CompleteOperations","CompleteOperations method [windows Media Format]","CompleteOperations method [windows Media Format]","IWMWriterFileSink3 interface","IWMWriterFileSink3 interface [windows Media Format]","CompleteOperations method","IWMWriterFileSink3.CompleteOperations","IWMWriterFileSink3::CompleteOperations","IWMWriterFileSink3CompleteOperations","wmformat.iwmwriterfilesink3_completeoperations","wmsdkidl/IWMWriterFileSink3::CompleteOperations"]
old-location: wmformat\iwmwriterfilesink3_completeoperations.htm
tech.root: wmformat
ms.assetid: 6eb4f09f-627e-4409-9f08-8f655aa7d0ec
ms.date: 12/05/2018
ms.keywords: CompleteOperations, CompleteOperations method [windows Media Format], CompleteOperations method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],CompleteOperations method, IWMWriterFileSink3.CompleteOperations, IWMWriterFileSink3::CompleteOperations, IWMWriterFileSink3CompleteOperations, wmformat.iwmwriterfilesink3_completeoperations, wmsdkidl/IWMWriterFileSink3::CompleteOperations
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
 - IWMWriterFileSink3::CompleteOperations
 - wmsdkidl/IWMWriterFileSink3::CompleteOperations
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
 - IWMWriterFileSink3.CompleteOperations
---

# IWMWriterFileSink3::CompleteOperations


## -description

The <b>CompleteOperations</b> method stops the writer sink after completing all operations in progress. This method is used with unbuffered I/O.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when writes are performed as a result of calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader">IWMWriterSink::OnHeader</a>, <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit">IWMWriterSink::OnDataUnit</a>, and <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-ondataunitex">IWMWriterFileSink3::OnDataUnitEx</a>. Applications do not call this method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setunbufferedio">IWMWriterFileSink3::SetUnbufferedIO</a>
