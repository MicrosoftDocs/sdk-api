---
UID: NF:vmr9.IVMRMixerControl9.SetOutputRect
title: IVMRMixerControl9::SetOutputRect
author: windows-sdk-content
description: The SetOutputRect method sets the position of this stream within the composition rectangle.
old-location: dshow\ivmrmixercontrol9_setoutputrect.htm
tech.root: DirectShow
ms.assetid: d09d2e90-e121-46e0-a659-e7bae4432031
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetOutputRect method, IVMRMixerControl9.SetOutputRect, IVMRMixerControl9::SetOutputRect, IVMRMixerControl9SetOutputRect, SetOutputRect, SetOutputRect method [DirectShow], SetOutputRect method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setoutputrect, vmr9/IVMRMixerControl9::SetOutputRect
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
 - IVMRMixerControl9.SetOutputRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vmr9.h
: 
- IVMRMixerControl9.SetOutputRect
: 
---

# IVMRMixerControl9::SetOutputRect


## -description



The <code>SetOutputRect</code> method sets the position of this stream within the composition rectangle.




## -parameters




### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.


### -param pRect [in]

Pointer to a <a href="https://msdn.microsoft.com/226b685c-92da-45c3-b99a-6c1e732f8dc6">VMR9NormalizedRect</a> structure that specifies the position of the rectangle with composition space.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
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



Because this rectangle exists in compositional space, there is no such thing as an "invalid" rectangle. For example, set left greater than right to mirror the video in the x direction. Specifying an empty rectangle turns off this stream.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

