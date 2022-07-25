---
UID: NF:dxgi1_4.IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent
title: IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent (dxgi1_4.h)
description: Registers to receive notification of hardware content protection teardown events.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","RegisterHardwareContentProtectionTeardownStatusEvent method","IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent","IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent","RegisterHardwareContentProtectionTeardownStatusEvent","RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI]","RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_registerhardwarecontentprotectionteardownstatusevent","dxgi1_4/IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent"]
old-location: direct3ddxgi\idxgiadapter3_registerhardwarecontentprotectionteardownstatusevent.htm
tech.root: direct3ddxgi
ms.assetid: 789E6EA1-C590-44F6-A474-851E5CF437A5
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],RegisterHardwareContentProtectionTeardownStatusEvent method, IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent, IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent, RegisterHardwareContentProtectionTeardownStatusEvent, RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI], RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_registerhardwarecontentprotectionteardownstatusevent, dxgi1_4/IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent
 - dxgi1_4/IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent
---

# IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent


## -description

Registers to receive notification of hardware content protection teardown events.

## -parameters

### -param hEvent [in]

Type: <b>HANDLE</b>

A handle to the event object that the operating system sets when hardware content protection teardown occurs. The <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function returns this handle.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a key value that an application can pass to the <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-unregisterhardwarecontentprotectionteardownstatus">IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus</a> method to unregister the notification event that <i>hEvent</i> specifies.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a>() to check for the presence of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_content_protection_caps">D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_TEARDOWN</a>  capability to know whether the hardware contains an automatic teardown mechanism.

After the event is signaled, the application can call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus">ID3D11VideoContext1::CheckCryptoSessionStatus</a> to determine the impact of the hardware teardown for a specific <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>