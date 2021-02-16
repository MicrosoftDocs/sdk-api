---
UID: NF:strmif.IAMExtDevice.get_ExternalDeviceID
title: IAMExtDevice::get_ExternalDeviceID (strmif.h)
description: The get_ExternalDeviceID method retrieves the model number of the external device.
helpviewer_keywords: ["IAMExtDevice interface [DirectShow]","get_ExternalDeviceID method","IAMExtDevice.get_ExternalDeviceID","IAMExtDevice::get_ExternalDeviceID","IAMExtDeviceget_ExternalDeviceID","dshow.iamextdevice_get_externaldeviceid","get_ExternalDeviceID","get_ExternalDeviceID method [DirectShow]","get_ExternalDeviceID method [DirectShow]","IAMExtDevice interface","strmif/IAMExtDevice::get_ExternalDeviceID"]
old-location: dshow\iamextdevice_get_externaldeviceid.htm
tech.root: dshow
ms.assetid: 2217b0b1-3663-438b-8951-d2d1d8404e9c
ms.date: 12/05/2018
ms.keywords: IAMExtDevice interface [DirectShow],get_ExternalDeviceID method, IAMExtDevice.get_ExternalDeviceID, IAMExtDevice::get_ExternalDeviceID, IAMExtDeviceget_ExternalDeviceID, dshow.iamextdevice_get_externaldeviceid, get_ExternalDeviceID, get_ExternalDeviceID method [DirectShow], get_ExternalDeviceID method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_ExternalDeviceID
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
 - IAMExtDevice::get_ExternalDeviceID
 - strmif/IAMExtDevice::get_ExternalDeviceID
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
 - IAMExtDevice.get_ExternalDeviceID
---

# IAMExtDevice::get_ExternalDeviceID


## -description

The <code>get_ExternalDeviceID</code> method retrieves the model number of the external device.

## -parameters

### -param ppszData [out]

Pointer to an <b>LPOLESTR</b> that receives the manufacturer-specific identification as a string. The caller must release the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>