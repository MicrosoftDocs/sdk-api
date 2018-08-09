---
UID: NF:videoacc.IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData
title: IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData
author: windows-sdk-content
description: The GetCreateVideoAcceleratorData method gets information needed to create a video accelerator object.
old-location: dshow\iamvideoacceleratornotify_getcreatevideoacceleratordata.htm
old-project: DirectShow
ms.assetid: 72e3331d-1e54-4ec7-9972-7e39eaf2707d
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetCreateVideoAcceleratorData, GetCreateVideoAcceleratorData method [DirectShow], GetCreateVideoAcceleratorData method [DirectShow],IAMVideoAcceleratorNotify interface, IAMVideoAcceleratorNotify interface [DirectShow],GetCreateVideoAcceleratorData method, IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData, IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData, IAMVideoAcceleratorNotifyGetCreateVideoAcceleratorData, dshow.iamvideoacceleratornotify_getcreatevideoacceleratordata, videoacc/IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAcceleratorNotify.GetCreateVideoAcceleratorData
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAMVideoAcceleratorNotify::GetCreateVideoAcceleratorData


## -description


The <b>GetCreateVideoAcceleratorData</b> method gets information needed to create a video accelerator object.


## -parameters




### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile in use.


### -param pdwSizeMiscData [out]

Receives the size of the data returned in <i>ppMiscData</i>, in bytes.
          


### -param ppMiscData [out]

Receives a pointer to a buffer that contains a <b>DXVA_ConnectMode</b>structure. The decoder must call <b>CoTaskMemAlloc</b> to allocate the memory for the structure. The caller must free the memory by calling <b>CoTaskMemFree</b>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/7fd0290c-8fd6-4af6-b510-7a87bc7937de">IAMVideoAcceleratorNotify Interface</a>
 

 

