---
UID: NF:mfidl.IMFMediaSourceEx.SetD3DManager
title: IMFMediaSourceEx::SetD3DManager
author: windows-sdk-content
description: Sets a pointer to the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the media source.
old-location: mf\imfmediasourceex_setd3dmanager.htm
tech.root: medfound
ms.assetid: 9E956E68-9950-4AA1-BF43-C1DCB02393F7
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaSourceEx interface [Media Foundation],SetD3DManager method, IMFMediaSourceEx.SetD3DManager, IMFMediaSourceEx::SetD3DManager, SetD3DManager, SetD3DManager method [Media Foundation], SetD3DManager method [Media Foundation],IMFMediaSourceEx interface, mf.imfmediasourceex_setd3dmanager, mfidl/IMFMediaSourceEx::SetD3DManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
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
 - mfidl.h
api_name:
 - IMFMediaSourceEx.SetD3DManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourceEx::SetD3DManager


## -description


Sets a pointer to the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the media source.


## -parameters




### -param pManager [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the DXGI Manager. The media source should query this pointer for the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> interface.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support source-level attributes.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/C72C79D5-FD65-4F27-A8C8-B94BF5A9E829">IMFMediaSourceEx</a>
 

 

