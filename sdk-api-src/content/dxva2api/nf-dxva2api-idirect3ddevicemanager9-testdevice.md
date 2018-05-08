---
UID: NF:dxva2api.IDirect3DDeviceManager9.TestDevice
title: IDirect3DDeviceManager9::TestDevice
author: windows-driver-content
description: Tests whether a Direct3D device handle is valid.
old-location: mf\idirect3ddevicemanager9_testdevice.htm
old-project: medfound
ms.assetid: e97acc5d-1b6a-43ae-a057-9c650d7126ab
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IDirect3DDeviceManager9 interface [Media Foundation],TestDevice method, IDirect3DDeviceManager9.TestDevice, IDirect3DDeviceManager9::TestDevice, TestDevice, TestDevice method [Media Foundation], TestDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::TestDevice, e97acc5d-1b6a-43ae-a057-9c650d7126ab, mf.idirect3ddevicemanager9_testdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirect3DDeviceManager9.TestDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDeviceManager9::TestDevice


## -description


Tests whether a Direct3D device handle is valid.
        


## -parameters




### -param hDevice [in]

Handle to a Direct3D device. To get a device handle, call <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">IDirect3DDeviceManager9::OpenDeviceHandle</a>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The device handle is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not a Direct3D device handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DXVA2_E_NEW_VIDEO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device handle is invalid.

</td>
</tr>
</table>
 




## -remarks



If the method returns DXVA2_E_NEW_VIDEO_DEVICE, call <a href="https://msdn.microsoft.com/5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a">IDirect3DDeviceManager9::CloseDeviceHandle</a> to close the handle and then call <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">OpenDeviceHandle</a> again to get a new handle. The <a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">IDirect3DDeviceManager9::ResetDevice</a> method invalidates all open device handles.




## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a>
 

 

