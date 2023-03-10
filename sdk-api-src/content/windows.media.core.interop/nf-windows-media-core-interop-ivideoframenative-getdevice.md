---
UID: NF:windows.media.core.interop.IVideoFrameNative.GetDevice
title: IVideoFrameNative::core (windows.media.core.interop.h)
description: This method returns a device associated with the video data.
helpviewer_keywords: ["GetDevice","GetDevice method [Windows Runtime]","GetDevice method [Windows Runtime]","IVideoFrameNative interface","IVideoFrameNative interface [Windows Runtime]","GetDevice method","IVideoFrameNative.GetDevice","IVideoFrameNative.core","IVideoFrameNative::GetDevice","IVideoFrameNative::core","windows/IVideoFrameNative::GetDevice","winrt.ivideoframenative_getdevice"]
old-location: winrt\ivideoframenative_getdevice.htm
tech.root: WinRT
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Windows Runtime], GetDevice method [Windows Runtime],IVideoFrameNative interface, IVideoFrameNative interface [Windows Runtime],GetDevice method, IVideoFrameNative.GetDevice, IVideoFrameNative.core, IVideoFrameNative::GetDevice, IVideoFrameNative::core, windows/IVideoFrameNative::GetDevice, winrt.ivideoframenative_getdevice
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
 - IVideoFrameNative::GetDevice
 - windows.media.core.interop/IVideoFrameNative::GetDevice
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
 - IVideoFrameNative.GetDevice
---

# IVideoFrameNative::core


## -description

This method returns a device associated with the video data.

## -parameters

### -param riid [in]

The IID of the device to retrieve.

### -param ppv [out]

When this method returns successfully, contains the device pointer requested in <i>riid</i> parameter.

## -returns

Returns S_OK on successful completion.

## -see-also

<a href="/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative">IVideoFrameNative</a>