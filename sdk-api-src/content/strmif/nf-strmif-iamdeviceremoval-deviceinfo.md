---
UID: NF:strmif.IAMDeviceRemoval.DeviceInfo
title: IAMDeviceRemoval::DeviceInfo (strmif.h)
description: The DeviceInfo method retrieves information about the device.
helpviewer_keywords: ["DeviceInfo","DeviceInfo method [DirectShow]","DeviceInfo method [DirectShow]","IAMDeviceRemoval interface","IAMDeviceRemoval interface [DirectShow]","DeviceInfo method","IAMDeviceRemoval.DeviceInfo","IAMDeviceRemoval::DeviceInfo","IAMDeviceRemovalDeviceInfo","dshow.iamdeviceremoval_deviceinfo","strmif/IAMDeviceRemoval::DeviceInfo"]
old-location: dshow\iamdeviceremoval_deviceinfo.htm
tech.root: dshow
ms.assetid: ec3628cf-fcb4-46c4-9de1-79bf1259c3db
ms.date: 4/26/2023
ms.keywords: DeviceInfo, DeviceInfo method [DirectShow], DeviceInfo method [DirectShow],IAMDeviceRemoval interface, IAMDeviceRemoval interface [DirectShow],DeviceInfo method, IAMDeviceRemoval.DeviceInfo, IAMDeviceRemoval::DeviceInfo, IAMDeviceRemovalDeviceInfo, dshow.iamdeviceremoval_deviceinfo, strmif/IAMDeviceRemoval::DeviceInfo
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
 - IAMDeviceRemoval::DeviceInfo
 - strmif/IAMDeviceRemoval::DeviceInfo
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
 - IAMDeviceRemoval.DeviceInfo
---

# IAMDeviceRemoval::DeviceInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DeviceInfo</code> method retrieves information about the device.

## -parameters

### -param pclsidInterfaceClass [out]

Receives a GUID that specifies the device interface class.

### -param pwszSymbolicLink [out]

Receives a pointer to a string that contains the Plug and Play (PnP) device path for the device. The caller must release the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the device interface classes and device paths, see Device I/O in the Windows SDK documentation.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdeviceremoval">IAMDeviceRemoval Interface</a>