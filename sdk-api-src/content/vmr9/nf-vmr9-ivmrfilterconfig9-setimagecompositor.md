---
UID: NF:vmr9.IVMRFilterConfig9.SetImageCompositor
title: IVMRFilterConfig9::SetImageCompositor
author: windows-sdk-content
description: The SetImageCompositor method installs an application-provided image compositor object.
old-location: dshow\ivmrfilterconfig9_setimagecompositor.htm
tech.root: DirectShow
ms.assetid: 8e4a66e8-d4ab-49e0-8773-c79b5965124b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetImageCompositor method, IVMRFilterConfig9.SetImageCompositor, IVMRFilterConfig9::SetImageCompositor, IVMRFilterConfig9SetImageCompositor, SetImageCompositor, SetImageCompositor method [DirectShow], SetImageCompositor method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setimagecompositor, vmr9/IVMRFilterConfig9::SetImageCompositor
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
 - IVMRFilterConfig9.SetImageCompositor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig9::SetImageCompositor


## -description



The <code>SetImageCompositor</code> method installs an application-provided image compositor object.




## -parameters




### -param lpVMRImgCompositor [in]

Pointer to the image compositor object provided by the application.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Cannot change the compositor when the VMR filter's pins are connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixing mode.

</td>
</tr>
</table>
 




## -remarks



Use this method to replace the VMR's default compositor with a custom compositor provided by the application. The image compositor is a sub-component of the mixer. The mixer must be loaded, through a call to <a href="https://msdn.microsoft.com/en-us/library/Dd377370(v=VS.85).aspx">IVMRFilterConfig9::SetNumberOfStreams</a>,

before the compositor can be specified. The VMR manages all reference counting on the <a href="https://msdn.microsoft.com/en-us/library/Dd377381(v=VS.85).aspx">IVMRImageCompositor9</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd377365(v=VS.85).aspx">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

