---
UID: NF:windows.media.core.interop.IAudioFrameNativeFactory.CreateFromMFSample
title: IAudioFrameNativeFactory::core (windows.media.core.interop.h)
description: Creates an IAudioFrameNative from the provided IMFSample.
old-location: winrt\iaudioframenativefactory_createfrommfsample.htm
tech.root: WinRT
ms.assetid: 331F6479-855E-459B-843F-B4FC4C88ED76
ms.date: 12/05/2018
ms.keywords: CreateFromMFSample, CreateFromMFSample method [Windows Runtime], CreateFromMFSample method [Windows Runtime],IAudioFrameNativeFactory interface, IAudioFrameNativeFactory interface [Windows Runtime],CreateFromMFSample method, IAudioFrameNativeFactory.CreateFromMFSample, IAudioFrameNativeFactory.core, IAudioFrameNativeFactory::CreateFromMFSample, IAudioFrameNativeFactory::core, windows/IAudioFrameNativeFactory::CreateFromMFSample, winrt.iaudioframenativefactory_createfrommfsample
ms.topic: method
f1_keywords:
- windows.media.core.interop/IAudioFrameNativeFactory.CreateFromMFSample
dev_langs:
- c++
req.header: windows.media.core.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- windows.media.core.interop.h
api_name:
- IAudioFrameNativeFactory.CreateFromMFSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioFrameNativeFactory::core


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative">IAudioFrameNative</a> from the provided <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>.


## -parameters




### -param data [in]

Type: <b>IMFSample*</b>

The source buffer containing an audio frame.


### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software audio frame is read-only.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative">IAudioFrameNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory">IAudioFrameNativeFactory</a>
 

 

