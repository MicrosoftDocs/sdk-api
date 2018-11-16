---
UID: NF:mfobjects.IMFDXGIBuffer.SetUnknown
title: IMFDXGIBuffer::SetUnknown
author: windows-sdk-content
description: Stores an arbitrary IUnknown pointer in the media buffer object.
old-location: mf\imfdxgibuffer_setunknown.htm
tech.root: medfound
ms.assetid: 94BA5E48-FF89-48FA-BE0D-C158A5B4D4CF
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFDXGIBuffer interface [Media Foundation],SetUnknown method, IMFDXGIBuffer.SetUnknown, IMFDXGIBuffer::SetUnknown, SetUnknown, SetUnknown method [Media Foundation], SetUnknown method [Media Foundation],IMFDXGIBuffer interface, mf.imfdxgibuffer_setunknown, mfobjects/IMFDXGIBuffer::SetUnknown
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
 - IMFDXGIBuffer.SetUnknown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMFDXGIBuffer.SetUnknown
: 
---

# IMFDXGIBuffer::SetUnknown


## -description


Stores an arbitrary <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer in the media buffer object.


## -parameters




### -param guid [in]

The identifier for the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer. This identifier is used as a key to retrieve the value. It can be any <b>GUID</b> value.


### -param pUnkData [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. Set this parameter to <b>NULL</b> to clear a pointer that was previously set.


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
<dt><b>ERROR_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
An item already exists with this key.

</td>
</tr>
</table>
 




## -remarks



To retrieve the pointer from the object, call <a href="https://msdn.microsoft.com/6B4A5E79-3A0A-439E-ABE1-F92C3D07FB57">IMFDXGIBuffer::GetUnknown</a>.




## -see-also




<a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a>



<a href="https://msdn.microsoft.com/6B4A5E79-3A0A-439E-ABE1-F92C3D07FB57">IMFDXGIBuffer::GetUnknown</a>
 

 

