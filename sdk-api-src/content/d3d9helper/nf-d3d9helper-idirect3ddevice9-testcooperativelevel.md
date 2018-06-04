---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DDevice9::TestCooperativeLevel


## -description


Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK, indicating that the device is operational and the calling application can continue.
 If the method fails, the return value can be one of the following values: D3DERR_DEVICELOST, D3DERR_DEVICENOTRESET, D3DERR_DRIVERINTERNALERROR.




## -remarks



If the device is lost but cannot be restored at the current time, <b>IDirect3DDevice9::TestCooperativeLevel</b> returns the D3DERR_DEVICELOST return code. This would be the case, for example, when a full-screen device has lost focus. If an application detects a lost device, it should pause and periodically call <b>IDirect3DDevice9::TestCooperativeLevel</b> until it receives a return value of D3DERR_DEVICENOTRESET. The application may then attempt to reset the device by calling <a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">IDirect3DDevice9::Reset</a> and, if this succeeds, restore the necessary resources and resume normal operation. Note that <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">IDirect3DDevice9::Present</a> will return D3DERR_DEVICELOST if the device is either "lost" or "not reset".

A call to <b>IDirect3DDevice9::TestCooperativeLevel</b> will fail if called on a different thread than that used to create the device being reset.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

