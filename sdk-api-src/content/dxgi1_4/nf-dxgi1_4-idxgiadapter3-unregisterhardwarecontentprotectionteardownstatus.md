---
UID: NF:dxgi1_4.IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus
title: IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus (dxgi1_4.h)
description: Unregisters an event to stop it from receiving notification of hardware content protection teardown events.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","UnregisterHardwareContentProtectionTeardownStatus method","IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus","IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus","UnregisterHardwareContentProtectionTeardownStatus","UnregisterHardwareContentProtectionTeardownStatus method [DXGI]","UnregisterHardwareContentProtectionTeardownStatus method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_unregisterhardwarecontentprotectionteardownstatus","dxgi1_4/IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus"]
old-location: direct3ddxgi\idxgiadapter3_unregisterhardwarecontentprotectionteardownstatus.htm
tech.root: direct3ddxgi
ms.assetid: 821F8BFA-FD11-4E3E-BE5A-05A1F1002EE6
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],UnregisterHardwareContentProtectionTeardownStatus method, IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus, IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus, UnregisterHardwareContentProtectionTeardownStatus, UnregisterHardwareContentProtectionTeardownStatus method [DXGI], UnregisterHardwareContentProtectionTeardownStatus method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_unregisterhardwarecontentprotectionteardownstatus, dxgi1_4/IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus
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
 - IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus
 - dxgi1_4/IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus
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
 - IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus
---

# IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus


## -description

Unregisters an event to stop it from receiving notification of hardware content protection teardown events.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

A key value for the window or event to unregister. The  <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a> method returns this value.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>