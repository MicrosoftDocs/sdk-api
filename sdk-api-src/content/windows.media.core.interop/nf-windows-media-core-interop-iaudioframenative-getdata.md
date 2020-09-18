---
UID: NF:windows.media.core.interop.IAudioFrameNative.GetData
title: IAudioFrameNative::core (windows.media.core.interop.h)
description: This method returns an interface that provides access to the audio data.
helpviewer_keywords: ["GetData","GetData method [Windows Runtime]","GetData method [Windows Runtime]","IAudioFrameNative interface","IAudioFrameNative interface [Windows Runtime]","GetData method","IAudioFrameNative.GetData","IAudioFrameNative.core","IAudioFrameNative::GetData","IAudioFrameNative::core","windows/IAudioFrameNative::GetData","winrt.iaudioframenative_getdata"]
old-location: winrt\iaudioframenative_getdata.htm
tech.root: WinRT
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Windows Runtime], GetData method [Windows Runtime],IAudioFrameNative interface, IAudioFrameNative interface [Windows Runtime],GetData method, IAudioFrameNative.GetData, IAudioFrameNative.core, IAudioFrameNative::GetData, IAudioFrameNative::core, windows/IAudioFrameNative::GetData, winrt.iaudioframenative_getdata
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioFrameNative::GetData
 - windows.media.core.interop/IAudioFrameNative::GetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.core.interop.h
api_name:
 - IAudioFrameNative.GetData
---

# IAudioFrameNative::core


## -description

This method returns an interface that provides access to the audio data.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface to retrieve.

### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion. Returns E_NOINTERFACE if the requested interface can't be found.

## -see-also

<a href="/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative">IAudioFrameNative</a>