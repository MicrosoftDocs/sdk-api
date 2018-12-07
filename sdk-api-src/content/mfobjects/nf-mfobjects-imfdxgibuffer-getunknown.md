---
UID: NF:mfobjects.IMFDXGIBuffer.GetUnknown
title: IMFDXGIBuffer::GetUnknown
author: windows-sdk-content
description: Gets an IUnknown pointer that was previously stored in the media buffer object.
old-location: mf\imfdxgibuffer_getunknown.htm
tech.root: medfound
ms.assetid: 6B4A5E79-3A0A-439E-ABE1-F92C3D07FB57
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUnknown, GetUnknown method [Media Foundation], GetUnknown method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetUnknown method, IMFDXGIBuffer.GetUnknown, IMFDXGIBuffer::GetUnknown, mf.imfdxgibuffer_getunknown, mfobjects/IMFDXGIBuffer::GetUnknown
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
 - IMFDXGIBuffer.GetUnknown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIBuffer::GetUnknown


## -description


Gets an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer that was previously stored in the media buffer object.


## -parameters




### -param guid [in]

The identifier of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer.


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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a>



<a href="https://msdn.microsoft.com/94BA5E48-FF89-48FA-BE0D-C158A5B4D4CF">IMFDXGIBuffer::SetUnknown</a>
 

 

