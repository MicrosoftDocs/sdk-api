---
UID: NF:vmr9.IVMRFilterConfig9.GetRenderingPrefs
title: IVMRFilterConfig9::GetRenderingPrefs
author: windows-sdk-content
description: The GetRenderingPrefs method retrieves the current set of rendering preferences being used by the VMR-9.
old-location: dshow\ivmrfilterconfig9_getrenderingprefs.htm
old-project: DirectShow
ms.assetid: b82a9dbe-aa86-4153-945b-fe8968faa5ca
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRFilterConfig9 interface, IVMRFilterConfig9 interface [DirectShow],GetRenderingPrefs method, IVMRFilterConfig9.GetRenderingPrefs, IVMRFilterConfig9::GetRenderingPrefs, IVMRFilterConfig9GetRenderingPrefs, dshow.ivmrfilterconfig9_getrenderingprefs, vmr9/IVMRFilterConfig9::GetRenderingPrefs
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
 - IVMRFilterConfig9.GetRenderingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRFilterConfig9::GetRenderingPrefs


## -description



The <b>GetRenderingPrefs</b> method retrieves the current set of rendering preferences being used by the VMR-9.




## -parameters




### -param pdwRenderFlags [out]

Receives a <a href="https://msdn.microsoft.com/a32119c2-a10d-41a0-b3e9-500323eb3094">VMR9RenderPrefs</a> value indicating the current rendering preferences.


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
The VMR has not created an allocator-presenter, or the allocator-presenter does not implement the <a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9</a> interface.

</td>
</tr>
</table>
 




## -remarks



If  the allocator-presenter implements the <a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9</a> interface, this method calls the <a href="https://msdn.microsoft.com/dfa9c81d-cfc8-401b-b4d1-50f21b528135">IVMRImagePresenterConfig9::GetRenderingPrefs</a> method on the allocator-presenter. 

The default allocator-presenter implements <a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9</a>. Custom allocator-presenters can also implements this interface if desired.

If the VMR-9 has not yet created the allocator-presenter, or if a custom allocator-presenter does not support <a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9</a>, this method returns <b>VFW_E_WRONG_STATE</b>. To create the default allocator-presenter, call <a href="https://msdn.microsoft.com/d7a27d7c-5cd4-4a20-ba15-7056d502e3e3">IVMRFilterConfig9::SetRenderingMode</a> with the value <b>VMR9Mode_Windowed</b> or <b>VMR9Mode_Windowless</b>.




## -see-also




<a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

