---
UID: NF:strmif.IAMExtDevice.get_ExternalDeviceVersion
title: IAMExtDevice::get_ExternalDeviceVersion (strmif.h)
description: The get_ExternalDeviceVersion retrieves the version number of the external device's operating software.
helpviewer_keywords: ["IAMExtDevice interface [DirectShow]","get_ExternalDeviceVersion method","IAMExtDevice.get_ExternalDeviceVersion","IAMExtDevice::get_ExternalDeviceVersion","IAMExtDeviceget_ExternalDeviceVersion","dshow.iamextdevice_get_externaldeviceversion","get_ExternalDeviceVersion","get_ExternalDeviceVersion method [DirectShow]","get_ExternalDeviceVersion method [DirectShow]","IAMExtDevice interface","strmif/IAMExtDevice::get_ExternalDeviceVersion"]
old-location: dshow\iamextdevice_get_externaldeviceversion.htm
tech.root: dshow
ms.assetid: 66a98ad3-850a-4b41-a169-f971fde83266
ms.date: 4/26/2023
ms.keywords: IAMExtDevice interface [DirectShow],get_ExternalDeviceVersion method, IAMExtDevice.get_ExternalDeviceVersion, IAMExtDevice::get_ExternalDeviceVersion, IAMExtDeviceget_ExternalDeviceVersion, dshow.iamextdevice_get_externaldeviceversion, get_ExternalDeviceVersion, get_ExternalDeviceVersion method [DirectShow], get_ExternalDeviceVersion method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_ExternalDeviceVersion
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtDevice::get_ExternalDeviceVersion
 - strmif/IAMExtDevice::get_ExternalDeviceVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtDevice.get_ExternalDeviceVersion
---

# IAMExtDevice::get_ExternalDeviceVersion


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ExternalDeviceVersion</code> retrieves the version number of the external device's operating software.

## -parameters

### -param ppszData [out]

Pointer to an <b>LPOLESTR</b> that receives the manufacturer-specific operating software version number as a string. The caller must release the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>