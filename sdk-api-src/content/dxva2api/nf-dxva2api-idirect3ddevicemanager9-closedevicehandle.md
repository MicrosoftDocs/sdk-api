---
UID: NF:dxva2api.IDirect3DDeviceManager9.CloseDeviceHandle
title: IDirect3DDeviceManager9::CloseDeviceHandle
author: windows-sdk-content
description: Closes a Direct3D device handle.
old-location: mf\idirect3ddevicemanager9_closedevicehandle.htm
tech.root: medfound
ms.assetid: 5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a, CloseDeviceHandle, CloseDeviceHandle method [Media Foundation], CloseDeviceHandle method [Media Foundation],IDirect3DDeviceManager9 interface, IDirect3DDeviceManager9 interface [Media Foundation],CloseDeviceHandle method, IDirect3DDeviceManager9.CloseDeviceHandle, IDirect3DDeviceManager9::CloseDeviceHandle, dxva2api/IDirect3DDeviceManager9::CloseDeviceHandle, mf.idirect3ddevicemanager9_closedevicehandle
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
 - IDirect3DDeviceManager9.CloseDeviceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDeviceManager9::CloseDeviceHandle


## -description


Closes a Direct3D device handle. Call this method to release a device handle retrieved by the <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">IDirect3DDeviceManager9::OpenDeviceHandle</a> method.
        
      


## -parameters




### -param hDevice [in]

Handle to the Direct3D device.


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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a>
 

 

