---
UID: NF:mfsharingengine.IMFMediaSharingEngine.GetDevice
title: IMFMediaSharingEngine::GetDevice (mfsharingengine.h)
description: Gets information about the media sharing device.
helpviewer_keywords: ["GetDevice","GetDevice method [Media Foundation]","GetDevice method [Media Foundation]","IMFMediaSharingEngine interface","IMFMediaSharingEngine interface [Media Foundation]","GetDevice method","IMFMediaSharingEngine.GetDevice","IMFMediaSharingEngine::GetDevice","mf.imfmediasharingengine_getdevice","mfsharingengine/IMFMediaSharingEngine::GetDevice"]
old-location: mf\imfmediasharingengine_getdevice.htm
tech.root: mf
ms.assetid: 29E536F3-E886-4DB6-8863-B4C0144FB693
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Media Foundation], GetDevice method [Media Foundation],IMFMediaSharingEngine interface, IMFMediaSharingEngine interface [Media Foundation],GetDevice method, IMFMediaSharingEngine.GetDevice, IMFMediaSharingEngine::GetDevice, mf.imfmediasharingengine_getdevice, mfsharingengine/IMFMediaSharingEngine::GetDevice
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFMediaSharingEngine::GetDevice
 - mfsharingengine/IMFMediaSharingEngine::GetDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IMFMediaSharingEngine.GetDevice
---

# IMFMediaSharingEngine::GetDevice


## -description

Gets information about the media sharing device.

## -parameters

### -param pDevice [out]

A pointer to a <a href="/windows/desktop/api/mfsharingengine/ns-mfsharingengine-device_info">DEVICE_INFO</a> structure. The method fills in this structure with the device information.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The method allocates memory for the <b>BSTR</b> members of the <a href="/windows/desktop/api/mfsharingengine/ns-mfsharingengine-device_info">DEVICE_INFO</a> structure. The caller must free the memory for each <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine">IMFMediaSharingEngine</a>