---
UID: NF:vmr9.IVMRDeinterlaceControl9.SetDeinterlaceMode
title: IVMRDeinterlaceControl9::SetDeinterlaceMode
author: windows-sdk-content
description: The SetDeinterlaceMode method sets the deinterlacing mode for the specified video stream.
old-location: dshow\ivmrdeinterlacecontrol9_setdeinterlacemode.htm
old-project: DirectShow
ms.assetid: 2c88b3b9-32eb-473b-9db5-9e9d65e2062c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRDeinterlaceControl9 interface [DirectShow],SetDeinterlaceMode method, IVMRDeinterlaceControl9.SetDeinterlaceMode, IVMRDeinterlaceControl9::SetDeinterlaceMode, IVMRDeinterlaceControl9SetDeinterlaceMode, SetDeinterlaceMode, SetDeinterlaceMode method [DirectShow], SetDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl9 interface, dshow.ivmrdeinterlacecontrol9_setdeinterlacemode, vmr9/IVMRDeinterlaceControl9::SetDeinterlaceMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRDeinterlaceControl9.SetDeinterlaceMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRDeinterlaceControl9::SetDeinterlaceMode


## -description



The <b>SetDeinterlaceMode</b> method sets the deinterlacing mode for the specified video stream.




## -parameters




### -param dwStreamID [in]

Index of the video stream to set. To set all streams, use the value 0xFFFFFFFF.


### -param lpDeinterlaceMode [in]

Pointer to a GUID that specifies the deinterlacing mode. To turn off deinterlacing, use the value GUID_NULL.


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



If the application does not specify the mode, the VMR defaults to the first mode reported by the driver. In either case, if the VMR cannot use the preferred mode, it falls back to another mode as specified in the <a href="https://msdn.microsoft.com/5d5b450f-bb87-41a2-bbb1-06b3956ba225">IVMRDeinterlaceControl9::SetDeinterlacePrefs</a> method.

The <b>SetDeinterlaceMode</b> method is effective only for new connections made to the VMR. Some deinterlacing mode require that additional reference samples be available; the exact number depends on the mode. The VMR allocates surfaces for these additional samples. The client must set the deinterlace mode before the surfaces have been allocated. Surface allocation occurs after any of the following:

<ul>
<li>Pin connections, including dynamic reconnections</li>
<li>Dynamic format changes (the upstream filter calls <a href="https://msdn.microsoft.com/b2013e95-88bc-4f4a-87af-2b13c120ec46">IPin::ReceiveConnection</a> to specify a new format)</li>
<li>Resolution changes</li>
<li>Monitor changes</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

