---
UID: NF:strmif.IVMRMixerControl.GetAlpha
title: IVMRMixerControl::GetAlpha
author: windows-sdk-content
description: The GetAlpha method retrieves the constant alpha value that is applied to this video stream.
old-location: dshow\ivmrmixercontrol_getalpha.htm
old-project: DirectShow
ms.assetid: a0a82a8f-a03a-43d7-8fb0-4c15b0cb7c27
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetAlpha, GetAlpha method [DirectShow], GetAlpha method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetAlpha method, IVMRMixerControl.GetAlpha, IVMRMixerControl::GetAlpha, IVMRMixerControlGetAlpha, dshow.ivmrmixercontrol_getalpha, strmif/IVMRMixerControl::GetAlpha
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl.GetAlpha
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::GetAlpha


## -description



The <code>GetAlpha</code> method retrieves the constant alpha value that is applied to this video stream.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param pAlpha [out]

Pointer to a variable of type float that receives the current alpha value.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pAlpha</i> is invalid.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/aab95d45-b8f1-40cb-811f-c1d00aa37c97">IVMRMixerControl::SetAlpha</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

