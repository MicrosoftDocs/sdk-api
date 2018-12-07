---
UID: NN:mfobjects.IMFDXGIBuffer
title: IMFDXGIBuffer
author: windows-sdk-content
description: Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.
old-location: mf\imfdxgibuffer.htm
tech.root: medfound
ms.assetid: 796D7755-275D-4A0B-A34F-5D34DCEC8AC7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFDXGIBuffer, IMFDXGIBuffer interface [Media Foundation], IMFDXGIBuffer interface [Media Foundation],described, mf.imfdxgibuffer, mfobjects/IMFDXGIBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IMFDXGIBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIBuffer interface


## -description


Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDXGIBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDXGIBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDXGIBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E8FF3346-D60A-4FF9-AF3E-673397EA6E6A">GetResource</a>
</td>
<td align="left" width="63%">
Queries the DXGIsurface for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71FA2B1C-2F11-45E7-8211-92A129F8C991">GetSubresourceIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the subresource that is associated with this media buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B4A5E79-3A0A-439E-ABE1-F92C3D07FB57">GetUnknown</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer that was previously stored in the media buffer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94BA5E48-FF89-48FA-BE0D-C158A5B4D4CF">SetUnknown</a>
</td>
<td align="left" width="63%">
Stores an arbitrary <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer in the media buffer object.

</td>
</tr>
</table> 


## -remarks



To create a DXGImedia buffer, first create the DXGIsurface. Then call <a href="https://msdn.microsoft.com/5D859F36-A82B-488B-A2F6-C697A1AA86BC">MFCreateDXGISurfaceBuffer</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

