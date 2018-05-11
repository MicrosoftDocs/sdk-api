---
UID: NF:dxva2api.IDirect3DDeviceManager9.UnlockDevice
title: IDirect3DDeviceManager9::UnlockDevice
author: windows-driver-content
description: Unlocks the Direct3D device.
old-location: mf\idirect3ddevicemanager9_unlockdevice.htm
old-project: medfound
ms.assetid: e5be74bc-55a2-4c8a-86eb-97b96a4091e7
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDirect3DDeviceManager9 interface [Media Foundation],UnlockDevice method, IDirect3DDeviceManager9.UnlockDevice, IDirect3DDeviceManager9::UnlockDevice, UnlockDevice, UnlockDevice method [Media Foundation], UnlockDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::UnlockDevice, e5be74bc-55a2-4c8a-86eb-97b96a4091e7, mf.idirect3ddevicemanager9_unlockdevice
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
-	IDirect3DDeviceManager9.UnlockDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDeviceManager9::UnlockDevice


## -description


Unlocks the Direct3D device. Call this method to release the device after calling <a href="https://msdn.microsoft.com/51631747-04af-448e-97cf-25a329d4fbb4">IDirect3DDeviceManager9::LockDevice</a>.


## -parameters




### -param hDevice [in]

Handle to the Direct3D device. To get the device handle, call <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">IDirect3DDeviceManager9::OpenDeviceHandle</a>.


### -param fSaveState [in]

If <b>TRUE</b>, the method saves the Direct3D device state in a state block. Internally, the method uses the Direct3D <b>IDirect3DStateBlock9</b> interface to save the device state. The next time you call <a href="https://msdn.microsoft.com/51631747-04af-448e-97cf-25a329d4fbb4">LockDevice</a> with the same device handle, the state block is restored.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is not locked, or is not a valid handle.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a>
 

 

