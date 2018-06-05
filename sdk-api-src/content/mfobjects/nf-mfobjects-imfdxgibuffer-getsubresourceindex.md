---
UID: NF:mfobjects.IMFDXGIBuffer.GetSubresourceIndex
title: IMFDXGIBuffer::GetSubresourceIndex
author: windows-sdk-content
description: Gets the index of the subresource that is associated with this media buffer.
old-location: mf\imfdxgibuffer_getsubresourceindex.htm
old-project: medfound
ms.assetid: 71FA2B1C-2F11-45E7-8211-92A129F8C991
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetSubresourceIndex, GetSubresourceIndex method [Media Foundation], GetSubresourceIndex method [Media Foundation],IMFDXGIBuffer interface, IMFDXGIBuffer interface [Media Foundation],GetSubresourceIndex method, IMFDXGIBuffer.GetSubresourceIndex, IMFDXGIBuffer::GetSubresourceIndex, mf.imfdxgibuffer_getsubresourceindex, mfobjects/IMFDXGIBuffer::GetSubresourceIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfobjects.h
api_name:
-	IMFDXGIBuffer.GetSubresourceIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDXGIBuffer::GetSubresourceIndex


## -description


Gets the index of the subresource that is associated with this media buffer.


## -parameters




### -param puSubresource [out]

Receives the zero-based index of the subresource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The subresource index is specified when you create the media buffer object. See <a href="https://msdn.microsoft.com/5D859F36-A82B-488B-A2F6-C697A1AA86BC">MFCreateDXGISurfaceBuffer</a>.

For more information about texture subresources, see <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>.




## -see-also




<a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a>
 

 

