---
UID: NF:videoacc.IAMVideoAcceleratorNotify.SetUncompSurfacesInfo
title: IAMVideoAcceleratorNotify::SetUncompSurfacesInfo
author: windows-sdk-content
description: The SetUncompSurfacesInfo method notifies the decoder of how many uncompressed surfaces were created.
old-location: dshow\iamvideoacceleratornotify_setuncompsurfacesinfo.htm
tech.root: DirectShow
ms.assetid: e82c73e6-d32e-4875-9f9d-124a1c6ce504
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMVideoAcceleratorNotify interface [DirectShow],SetUncompSurfacesInfo method, IAMVideoAcceleratorNotify.SetUncompSurfacesInfo, IAMVideoAcceleratorNotify::SetUncompSurfacesInfo, IAMVideoAcceleratorNotifySetUncompSurfacesInfo, SetUncompSurfacesInfo, SetUncompSurfacesInfo method [DirectShow], SetUncompSurfacesInfo method [DirectShow],IAMVideoAcceleratorNotify interface, dshow.iamvideoacceleratornotify_setuncompsurfacesinfo, videoacc/IAMVideoAcceleratorNotify::SetUncompSurfacesInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAcceleratorNotify.SetUncompSurfacesInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAcceleratorNotify::SetUncompSurfacesInfo


## -description


The <b>SetUncompSurfacesInfo</b> method notifies the decoder of how many uncompressed surfaces were created.


## -parameters




### -param dwActualUncompSurfacesAllocated [in]

The number of surfaces allocated.
          


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>
 




## -remarks



The video renderer calls this method after it allocates uncompressed surfaces for video decoding.




## -see-also




<a href="https://msdn.microsoft.com/5fd72be3-4ff5-4c93-8055-abe247f3c856">DirectShow Reference</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/7fd0290c-8fd6-4af6-b510-7a87bc7937de">IAMVideoAcceleratorNotify Interface</a>
 

 

