---
UID: NF:strmif.IVMRMixerControl.SetAlpha
title: IVMRMixerControl::SetAlpha
author: windows-sdk-content
description: The SetAlpha method sets a constant alpha value that is applied to this video stream.
old-location: dshow\ivmrmixercontrol_setalpha.htm
old-project: DirectShow
ms.assetid: aab95d45-b8f1-40cb-811f-c1d00aa37c97
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IVMRMixerControl interface [DirectShow],SetAlpha method, IVMRMixerControl.SetAlpha, IVMRMixerControl::SetAlpha, IVMRMixerControlSetAlpha, SetAlpha, SetAlpha method [DirectShow], SetAlpha method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setalpha, strmif/IVMRMixerControl::SetAlpha
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMixerControl.SetAlpha
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::SetAlpha


## -description



The <code>SetAlpha</code> method sets a constant alpha value that is applied to this video stream.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param Alpha [in]

Specifies the alpha blending value to be applied to all the pixels in this stream.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>
 




## -remarks



The alpha value specified can be between 0.0 (fully transparent) and 1.0 (full opaque).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/a0a82a8f-a03a-43d7-8fb0-4c15b0cb7c27">IVMRMixerControl::GetAlpha</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

