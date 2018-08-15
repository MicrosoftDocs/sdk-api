---
UID: NN:dxva2api.IDirectXVideoDecoder
title: IDirectXVideoDecoder
author: windows-sdk-content
description: Represents a DirectX Video Acceleration (DXVA) video decoder device.
old-location: mf\idirectxvideodecoder.htm
old-project: medfound
ms.assetid: 116c19a3-39be-4f96-969f-f3d62ed33a70
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 116c19a3-39be-4f96-969f-f3d62ed33a70, IDirectXVideoDecoder, IDirectXVideoDecoder interface [Media Foundation], IDirectXVideoDecoder interface [Media Foundation],described, dxva2api/IDirectXVideoDecoder, mf.idirectxvideodecoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxva2api.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXVA2_SurfaceType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoDecoder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoDecoder interface


## -description


Represents a DirectX Video Acceleration (DXVA) video decoder device.

 To get a pointer to this interface, call <a href="https://msdn.microsoft.com/2a799411-e8d5-4ab8-b52f-7198af9a4f2b">IDirectXVideoDecoderService::CreateVideoDecoder</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectXVideoDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17759e7b-e6d4-4270-abd3-0f73c1df7ccb">BeginFrame</a>
</td>
<td align="left" width="63%">
Starts the decoding operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b8d391e-b679-4adb-8b01-2899996ede46">EndFrame</a>
</td>
<td align="left" width="63%">
Signals the end of the decoding operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">Execute</a>
</td>
<td align="left" width="63%">
Executes a decoding operation on the current frame.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db2d4818-8a96-461e-88c4-f25d3200d815">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a pointer to a DXVA decoder buffer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e1a4f6b-22f3-40ae-8990-88ecb5b16d44">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Gets the parameters that were used to create this device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092c49cd-6bfc-4ed0-9378-5751ad19296c">GetVideoDecoderService</a>
</td>
<td align="left" width="63%">
Gets the DXVA decoder service that created this decoder device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a buffer that was obtained by calling <a href="https://msdn.microsoft.com/db2d4818-8a96-461e-88c4-f25d3200d815">GetBuffer</a>.
        

</td>
</tr>
</table> 


## -remarks



The <b>IDirectXVideoDecoder</b> methods make calls to the Direct3D device. Therefore, the <b>D3DCREATE</b> flags that you specify  when creating the device can affect the behavior of this interface. For example, if you specify the <b>D3DCREATE_MULTITHREADED</b> flag, the Direct3D global critical section will be held during decode operations.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

