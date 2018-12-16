---
UID: NF:videoacc.IAMVideoAccelerator.GetVideoAcceleratorGUIDs
title: IAMVideoAccelerator::GetVideoAcceleratorGUIDs
author: windows-sdk-content
description: The GetVideoAcceleratorGUIDs method gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.
old-location: dshow\iamvideoaccelerator_getvideoacceleratorguids.htm
tech.root: DirectShow
ms.assetid: 808ba120-f0e1-4348-94e7-69a27c77cf42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVideoAcceleratorGUIDs, GetVideoAcceleratorGUIDs method [DirectShow], GetVideoAcceleratorGUIDs method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetVideoAcceleratorGUIDs method, IAMVideoAccelerator.GetVideoAcceleratorGUIDs, IAMVideoAccelerator::GetVideoAcceleratorGUIDs, IAMVideoAcceleratorGetVideoAcceleratorGUIDs, dshow.iamvideoaccelerator_getvideoacceleratorguids, videoacc/IAMVideoAccelerator::GetVideoAcceleratorGUIDs
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
 - IAMVideoAccelerator.GetVideoAcceleratorGUIDs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAccelerator::GetVideoAcceleratorGUIDs


## -description



The <b>GetVideoAcceleratorGUIDs</b> method gets a list of DirectX Video Acceleration (DXVA) profiles supported by the display driver.




## -parameters




### -param pdwNumGuidsSupported [in, out]

On input, specifies the number of elements in the <i>pGuidsSupported</i> array.
            If <i>pGuidsSupported</i> is <b>NULL</b>, the value of <code>*pdwNumGuidsSupported</code> must be zero. 

On output, if <i>pGuidsSupported</i> is <b>NULL</b>, <i>pdwNumGuidsSupported</i> receives the number of restricted-mode DXVA profiles. Otherwise, <i>pdwNumGuidsSupported</i> receives the actual number of GUIDs copied to the <i>pGuidsSupported</i> array.


### -param pGuidsSupported [in, out]

Address of an array of GUIDs, or <b>NULL</b>. If the value is non-<b>NULL</b>, the array receives a list of GUIDs that specify restricted-mode DXVA profiles. These GUIDs are defined in the header file dxva.h, and are documented in the <a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>.


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
The method is not supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Invalid state. The video renderer has not created the Direct3D or DirectDraw device.

</td>
</tr>
</table>
 




## -remarks



Call this method twice. On the first call, set <i>pGuidsSupported</i> to <b>NULL</b>. The <i>pdwNumGuidsSupported</i> parameter receives the number of DXVA profile GUIDs. Allocate an array of GUIDs with the required size and call the method again. This time, set <i>pGuidsSupported</i> to the address of the array. The method fills the array with the list of DXVA profile GUIDs.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd375992(v=VS.85).aspx">IAMVideoAccelerator Interface</a>
 

 

