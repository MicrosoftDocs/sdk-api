---
UID: NF:wmsdkidl.IWMReader.Resume
title: IWMReader::Resume (wmsdkidl.h)
description: The Resume method starts the reader from the current position, after a Pause method call.
helpviewer_keywords: ["IWMReader interface [windows Media Format]","Resume method","IWMReader.Resume","IWMReader::Resume","IWMReaderResume","Resume","Resume method [windows Media Format]","Resume method [windows Media Format]","IWMReader interface","wmformat.iwmreader_resume","wmsdkidl/IWMReader::Resume"]
old-location: wmformat\iwmreader_resume.htm
tech.root: wmformat
ms.assetid: 4af00d1f-c78a-4f43-be2d-9561e3c7cf36
ms.date: 12/05/2018
ms.keywords: IWMReader interface [windows Media Format],Resume method, IWMReader.Resume, IWMReader::Resume, IWMReaderResume, Resume, Resume method [windows Media Format], Resume method [windows Media Format],IWMReader interface, wmformat.iwmreader_resume, wmsdkidl/IWMReader::Resume
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
 - IWMReader::Resume
 - wmsdkidl/IWMReader::Resume
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
 - IWMReader.Resume
---

# IWMReader::Resume


## -description

The <b>Resume</b> method starts the reader from the current position, after a <b>Pause</b> method call.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>
