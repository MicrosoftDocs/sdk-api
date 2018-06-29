---
UID: NF:dxgi1_4.IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent
title: IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent
author: windows-sdk-content
description: Registers to receive notification of hardware content protection teardown events.
old-location: direct3ddxgi\idxgiadapter3_registerhardwarecontentprotectionteardownstatusevent.htm
old-project: direct3ddxgi
ms.assetid: 789E6EA1-C590-44F6-A474-851E5CF437A5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],RegisterHardwareContentProtectionTeardownStatusEvent method, IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent, IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent, RegisterHardwareContentProtectionTeardownStatusEvent, RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI], RegisterHardwareContentProtectionTeardownStatusEvent method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_registerhardwarecontentprotectionteardownstatusevent, dxgi1_4/IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.RegisterHardwareContentProtectionTeardownStatusEvent
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent


## -description


Registers to receive notification of hardware content protection teardown events.


## -parameters




### -param hEvent [in]

Type: <b>HANDLE</b>

A handle to the event object that the operating system sets when hardware content protection teardown occurs. The <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function returns this handle. 


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a key value that an application can pass to the <a href="https://msdn.microsoft.com/821F8BFA-FD11-4E3E-BE5A-05A1F1002EE6">IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus</a> method to unregister the notification event that <i>hEvent</i> specifies.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <a href="https://msdn.microsoft.com/3BF2D2B9-6A12-4E71-9F52-829BABA32EF6">ID3D11VideoDevice::GetContentProtectionCaps</a>() to check for the presence of the <a href="https://msdn.microsoft.com/19697660-DDB8-4A4C-888F-018BC5CCFC94">D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_TEARDOWN</a>  capability to know whether the hardware contains an automatic teardown mechanism.

After the event is signaled, the application can call <a href="https://msdn.microsoft.com/07126C45-2771-432C-9644-FD4099B8D26D">ID3D11VideoContext1::CheckCryptoSessionStatus</a> to determine the impact of the hardware teardown for a specific <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface.





## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

