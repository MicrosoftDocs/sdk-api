---
UID: NF:mfidl.IMFTimecodeTranslate.EndConvertTimecodeToHNS
title: IMFTimecodeTranslate::EndConvertTimecodeToHNS (mfidl.h)
description: Completes an asynchronous request to convert time in Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.
helpviewer_keywords: ["EndConvertTimecodeToHNS","EndConvertTimecodeToHNS method [Media Foundation]","EndConvertTimecodeToHNS method [Media Foundation]","IMFTimecodeTranslate interface","IMFTimecodeTranslate interface [Media Foundation]","EndConvertTimecodeToHNS method","IMFTimecodeTranslate.EndConvertTimecodeToHNS","IMFTimecodeTranslate::EndConvertTimecodeToHNS","mf.imftimecodetranslate_endconverttimecodetohns","mfidl/IMFTimecodeTranslate::EndConvertTimecodeToHNS"]
old-location: mf\imftimecodetranslate_endconverttimecodetohns.htm
tech.root: mf
ms.assetid: d1b8b8ba-d03a-4a45-8788-38dbb2be8c6a
ms.date: 12/05/2018
ms.keywords: EndConvertTimecodeToHNS, EndConvertTimecodeToHNS method [Media Foundation], EndConvertTimecodeToHNS method [Media Foundation],IMFTimecodeTranslate interface, IMFTimecodeTranslate interface [Media Foundation],EndConvertTimecodeToHNS method, IMFTimecodeTranslate.EndConvertTimecodeToHNS, IMFTimecodeTranslate::EndConvertTimecodeToHNS, mf.imftimecodetranslate_endconverttimecodetohns, mfidl/IMFTimecodeTranslate::EndConvertTimecodeToHNS
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimecodeTranslate::EndConvertTimecodeToHNS
 - mfidl/IMFTimecodeTranslate::EndConvertTimecodeToHNS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTimecodeTranslate.EndConvertTimecodeToHNS
---

# IMFTimecodeTranslate::EndConvertTimecodeToHNS


## -description

Completes an asynchronous request to convert time in Society of Motion Picture and Television Engineers (SMPTE) time code to 100-nanosecond units.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

### -param phnsTime [out]

Receives the converted time.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method after the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns">IMFTimecodeTranslate::BeginConvertTimecodeToHNS</a> method completes asynchronously.

## -see-also

<a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate">IMFTimecodeTranslate</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>