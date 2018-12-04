---
UID: NF:vmr9.IVMRDeinterlaceControl9.GetDeinterlaceMode
title: IVMRDeinterlaceControl9::GetDeinterlaceMode
author: windows-sdk-content
description: The GetDeinterlaceMode method retrieves the deinterlacing mode for the specified video stream.
old-location: dshow\ivmrdeinterlacecontrol9_getdeinterlacemode.htm
tech.root: DirectShow
ms.assetid: 64cdba05-3f09-4fce-be38-9ee494018974
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetDeinterlaceMode, GetDeinterlaceMode method [DirectShow], GetDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl9 interface, IVMRDeinterlaceControl9 interface [DirectShow],GetDeinterlaceMode method, IVMRDeinterlaceControl9.GetDeinterlaceMode, IVMRDeinterlaceControl9::GetDeinterlaceMode, IVMRDeinterlaceControl9GetDeinterlaceMode, dshow.ivmrdeinterlacecontrol9_getdeinterlacemode, vmr9/IVMRDeinterlaceControl9::GetDeinterlaceMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRDeinterlaceControl9.GetDeinterlaceMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRDeinterlaceControl9::GetDeinterlaceMode


## -description



The <b>GetDeinterlaceMode</b> method retrieves the deinterlacing mode for the specified video stream.




## -parameters




### -param dwStreamID [in]

Index of the video stream to check.


### -param lpDeinterlaceMode [out]

Pointer to a variable that receives a GUID. The GUID identifies the deinterlacing mode currently in use. If no deinterlacing mode was set, or the pin corresponding to the stream ID is not connected to an interlaced stream, the value is GUID_NULL.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No deinterlacing mode was set.

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
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>
 




## -remarks



The VMR may not be able to use the requested mode, in which case it falls back to another deinterlace mode, as specified in the <a href="https://msdn.microsoft.com/5d5b450f-bb87-41a2-bbb1-06b3956ba225">IVMRDeinterlaceControl9::SetDeinterlacePrefs</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

