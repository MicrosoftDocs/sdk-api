---
UID: NF:windows.media.core.interop.IVideoFrameNative.GetData
title: IVideoFrameNative::core (windows.media.core.interop.h)
description: This method returns an interface that provides access to the video data.
helpviewer_keywords: ["GetData","GetData method [Windows Runtime]","GetData method [Windows Runtime]","IVideoFrameNative interface","IVideoFrameNative interface [Windows Runtime]","GetData method","IVideoFrameNative.GetData","IVideoFrameNative.core","IVideoFrameNative::GetData","IVideoFrameNative::core","windows/IVideoFrameNative::GetData","winrt.ivideoframenative_getdata"]
old-location: winrt\ivideoframenative_getdata.htm
tech.root: WinRT
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Windows Runtime], GetData method [Windows Runtime],IVideoFrameNative interface, IVideoFrameNative interface [Windows Runtime],GetData method, IVideoFrameNative.GetData, IVideoFrameNative.core, IVideoFrameNative::GetData, IVideoFrameNative::core, windows/IVideoFrameNative::GetData, winrt.ivideoframenative_getdata
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
 - IVideoFrameNative::GetData
 - windows.media.core.interop/IVideoFrameNative::GetData
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
 - IVideoFrameNative.GetData
---

# IVideoFrameNative::core


## -description

This method returns an interface that provides access to the video data.

## -parameters

### -param riid [in]

The IID of the interface to retrieve.

### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i> parameter.

## -returns

Returns S_OK on successful completion. Returns E_NOINTERFACE if the requested interface can't be found.

## -see-also

<a href="/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative">IVideoFrameNative</a>