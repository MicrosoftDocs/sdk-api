---
UID: NF:vmr9.IVMRFilterConfig9.SetRenderingPrefs
title: IVMRFilterConfig9::SetRenderingPrefs
author: windows-sdk-content
description: The SetRenderingPrefs method sets various application preferences related to video rendering.
old-location: dshow\ivmrfilterconfig9_setrenderingprefs.htm
tech.root: DirectShow
ms.assetid: ce274528-c759-4b43-80c7-0ba1e1275b7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetRenderingPrefs method, IVMRFilterConfig9.SetRenderingPrefs, IVMRFilterConfig9::SetRenderingPrefs, IVMRFilterConfig9SetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setrenderingprefs, vmr9/IVMRFilterConfig9::SetRenderingPrefs
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
 - IVMRFilterConfig9.SetRenderingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig9::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets various application preferences related to video rendering.




## -parameters




### -param dwRenderFlags [in]

Double word containing a bitwise OR of <a href="https://msdn.microsoft.com/en-us/library/Dd407375(v=VS.85).aspx">VMR9RenderPrefs</a> values specifying the rendering preferences.


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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
No allocator-presenter is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwRenderFlags</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



This method calls through to the allocator-presenter's <a href="https://msdn.microsoft.com/en-us/library/Dd377398(v=VS.85).aspx">IVMRImagePresenterConfig9::SetRenderingPrefs</a> method. (The default allocator-presenter exposes <b>IVMRImagePresenterConfig9</b>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-9 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig9</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="https://msdn.microsoft.com/en-us/library/Dd377371(v=VS.85).aspx">IVMRFilterConfig9::SetRenderingMode</a> with the value VMR9Mode_Windowed or VMR9Mode_Windowed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd377365(v=VS.85).aspx">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

