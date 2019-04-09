---
UID: NF:strmif.IVMRMixerControl.SetOutputRect
title: IVMRMixerControl::SetOutputRect (strmif.h)
author: windows-sdk-content
description: The SetOutputRect method sets the position of this stream within the composition rectangle.
old-location: dshow\ivmrmixercontrol_setoutputrect.htm
tech.root: DirectShow
ms.assetid: e7e1689c-03b4-457e-8d4c-6d59a70c42af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl interface [DirectShow],SetOutputRect method, IVMRMixerControl.SetOutputRect, IVMRMixerControl::SetOutputRect, IVMRMixerControlSetMixingPrefs, SetOutputRect, SetOutputRect method [DirectShow], SetOutputRect method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setoutputrect, strmif/IVMRMixerControl::SetOutputRect
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
 - IVMRMixerControl.SetOutputRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerControl::SetOutputRect


## -description



The <code>SetOutputRect</code> method sets the position of this stream within the composition rectangle.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param pRect [in]

Pointer to a <a href="https://msdn.microsoft.com/c40a0feb-f33e-40e3-9c58-0a22d2aa1858">NORMALIZEDRECT</a> structure that specifies the position of the rectangle with composition space.


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



Because this rectangle exists in compositional space, there is no such thing as an "invalid" rectangle. For example, set left greater than right to mirror the video in the x direction. Specifying an empty rectangle turns off this stream.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/da6409b0-161d-4724-b448-e68cb5d1941c">IVMRMixerControl::GetOutputRect</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

