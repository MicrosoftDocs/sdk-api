---
UID: NN:dxva2api.IDirect3DDeviceManager9
title: IDirect3DDeviceManager9
author: windows-sdk-content
description: Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.
old-location: mf\idirect3ddevicemanager9.htm
tech.root: medfound
ms.assetid: e661e666-dc51-4a71-9ecd-62a667bb217d
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IDirect3DDeviceManager9, IDirect3DDeviceManager9 interface [Media Foundation], IDirect3DDeviceManager9 interface [Media Foundation],described, dxva2api/IDirect3DDeviceManager9, e661e666-dc51-4a71-9ecd-62a667bb217d, mf.idirect3ddevicemanager9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirect3DDeviceManager9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDeviceManager9 interface


## -description


Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDeviceManager9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DDeviceManager9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDeviceManager9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a">CloseDeviceHandle</a>
</td>
<td align="left" width="63%">
Closes a Direct3D device handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e62a750-3017-4dd7-9fbc-e2c641f6cf10">GetVideoService</a>
</td>
<td align="left" width="63%">
Gets a DirectX Video Acceleration (DXVA) service interface.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51631747-04af-448e-97cf-25a329d4fbb4">LockDevice</a>
</td>
<td align="left" width="63%">
Gives the caller exclusive access to the Direct3D device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">OpenDeviceHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the Direct3D device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">ResetDevice</a>
</td>
<td align="left" width="63%">
Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e97acc5d-1b6a-43ae-a057-9c650d7126ab">TestDevice</a>
</td>
<td align="left" width="63%">
Tests whether a Direct3D device handle is valid.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5be74bc-55a2-4c8a-86eb-97b96a4091e7">UnlockDevice</a>
</td>
<td align="left" width="63%">
Unlocks the Direct3D device.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the <a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>. To create the Direct3D device manager, call <a href="https://msdn.microsoft.com/b06e9c68-80ee-4997-bcf7-f05879aa5776">DXVA2CreateDirect3DDeviceManager9</a>.

To get this interface from the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR), call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service GUID is <b>MR_VIDEO_ACCELERATION_SERVICE</b>. For the DirectShow EVR filter, call <b>GetService</b> on the filter's pins.

The Direct3D Device Manager supports Direct3D 9 devices only. It does not support DXGI devices.

Windows Store apps must use <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> and <a href="https://msdn.microsoft.com/7C91BEB9-53D2-4799-98F8-2B92128E37C3">Direct3D 11 Video APIs</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

