---
UID: NF:strmif.IVMRMixerControl.GetOutputRect
title: IVMRMixerControl::GetOutputRect
author: windows-sdk-content
description: The GetOutputRect method retrieves the position of this stream's video rectangle within the composition rectangle.
old-location: dshow\ivmrmixercontrol_getoutputrect.htm
old-project: DirectShow
ms.assetid: da6409b0-161d-4724-b448-e68cb5d1941c
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetOutputRect, GetOutputRect method [DirectShow], GetOutputRect method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetOutputRect method, IVMRMixerControl.GetOutputRect, IVMRMixerControl::GetOutputRect, IVMRMixerControlGetOutputRect, dshow.ivmrmixercontrol_getoutputrect, strmif/IVMRMixerControl::GetOutputRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
 - IVMRMixerControl.GetOutputRect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::GetOutputRect


## -description



The <code>GetOutputRect</code> method retrieves the position of this stream's video rectangle within the composition rectangle.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param pRect [out]

Pointer to a <a href="https://msdn.microsoft.com/c40a0feb-f33e-40e3-9c58-0a22d2aa1858">NORMALIZEDRECT</a> structure that receives the destination rectangle in composition space.


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
<i>pRect</i> is invalid.

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
 




## -remarks



Because this rectangle exists in compositional space, there is no such thing as an "invalid" rectangle. For example, if left is greater than right, it means the video is mirrored in the x direction. An empty rectangle turns off this stream.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/b0bd2086-af22-4530-921d-b7c56471d142">IVMRMixerControl::SetOutputRect</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

