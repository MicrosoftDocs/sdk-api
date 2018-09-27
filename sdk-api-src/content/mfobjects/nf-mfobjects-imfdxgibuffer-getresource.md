---
UID: NF:mfobjects.IMFDXGIBuffer.GetResource
title: IMFDXGIBuffer::GetResource
author: windows-sdk-content
description: Queries the Microsoft DirectX Graphics Infrastructure (DXGI)surface for an interface.
old-location: mf\imfdxgibuffer_getresource.htm
tech.root: medfound
ms.assetid: E8FF3346-D60A-4FF9-AF3E-673397EA6E6A
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetResource, GetResource method [Media Foundation], GetResource method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetResource method, IMFDXGIBuffer.GetResource, IMFDXGIBuffer::GetResource, mf.imfdxgibuffer_getresource, mfobjects/IMFDXGIBuffer::GetResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - IMFDXGIBuffer.GetResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIBuffer::GetResource


## -description


Queries the Microsoft DirectX Graphics Infrastructure (DXGI)surface for an interface.


## -parameters




### -param riid [in]

The interface identifer (IID) of the interface being requested.


### -param ppvObject [out]

Receives a pointer to the interface. The caller must release the interface.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
</table>
 




## -remarks



You can use this method to get a pointer to the <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a> interface of the surface. If the buffer is locked, the method returns <b>MF_E_INVALIDREQUEST</b>.




## -see-also




<a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a>
 

 

