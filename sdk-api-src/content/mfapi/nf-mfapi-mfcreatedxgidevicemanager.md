---
UID: NF:mfapi.MFCreateDXGIDeviceManager
title: MFCreateDXGIDeviceManager function
author: windows-driver-content
description: Creates an instance of the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
old-location: mf\mfcreatedxgidevicemanager.htm
old-project: medfound
ms.assetid: 5398B6D7-1E7D-4987-A163-3360C805EE9C
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MFCreateDXGIDeviceManager, MFCreateDXGIDeviceManager function [Media Foundation], mf.mfcreatedxgidevicemanager, mfapi/MFCreateDXGIDeviceManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateDXGIDeviceManager
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateDXGIDeviceManager function


## -description


Creates an instance of the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.


## -parameters




### -param resetToken

TBD


### -param ppDeviceManager

TBD




#### - pResetToken [out]


            Receives a token that identifies this instance of the DXGI Device Manager. Use this token when calling <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>.
          


#### - ppDXVAManager [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When you create an <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> with <b>MFCreateDXGIDeviceManager</b>, a Microsoft Direct3D 11 device is not associated with the device manager. To associate a Direct3D 11 device with the device manager, call <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>, passing in the pointer to the Direct3D 11 device. To create a Direct3D 11 device, call <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>. The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_FLAG</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

