---
UID: NF:dxva2api.IDirect3DDeviceManager9.OpenDeviceHandle
title: IDirect3DDeviceManager9::OpenDeviceHandle (dxva2api.h)
author: windows-sdk-content
description: Gets a handle to the Direct3D device.
old-location: mf\idirect3ddevicemanager9_opendevicehandle.htm
tech.root: medfound
ms.assetid: 74cd2260-279a-4956-8fce-40f8008b6797
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 74cd2260-279a-4956-8fce-40f8008b6797, IDirect3DDeviceManager9 interface [Media Foundation],OpenDeviceHandle method, IDirect3DDeviceManager9.OpenDeviceHandle, IDirect3DDeviceManager9::OpenDeviceHandle, OpenDeviceHandle, OpenDeviceHandle method [Media Foundation], OpenDeviceHandle method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::OpenDeviceHandle, mf.idirect3ddevicemanager9_opendevicehandle
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
 - IDirect3DDeviceManager9.OpenDeviceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDeviceManager9::OpenDeviceHandle


## -description


Gets a handle to the Direct3D device.
        


## -parameters




### -param phDevice [out]

Receives the device handle.


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
<dt><b>DXVA2_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Direct3D device manager was not initialized. The owner of the device must call <a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">IDirect3DDeviceManager9::ResetDevice</a>.

</td>
</tr>
</table>
 




## -remarks



To get the Direct3D device's <b>IDirect3DDevice9</b> pointer, call <a href="https://msdn.microsoft.com/51631747-04af-448e-97cf-25a329d4fbb4">IDirect3DDeviceManager9::LockDevice</a> with the handle returned in <i>phDevice</i>. Close the device handle when you are done using it, by calling <a href="https://msdn.microsoft.com/5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a">IDirect3DDeviceManager9::CloseDeviceHandle</a>.

To test whether a device handle is still valid, call <a href="https://msdn.microsoft.com/e97acc5d-1b6a-43ae-a057-9c650d7126ab">IDirect3DDeviceManager9::TestDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a>
 

 

