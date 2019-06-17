---
UID: NF:vmr9.IVMRImagePresenterConfig9.GetRenderingPrefs
title: IVMRImagePresenterConfig9::GetRenderingPrefs (vmr9.h)
author: windows-sdk-content
description: The GetRenderingPrefs method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.
old-location: dshow\ivmrimagepresenterconfig9_getrenderingprefs.htm
tech.root: DirectShow
ms.assetid: dfa9c81d-cfc8-401b-b4d1-50f21b528135
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig9 interface, IVMRImagePresenterConfig9 interface [DirectShow],GetRenderingPrefs method, IVMRImagePresenterConfig9.GetRenderingPrefs, IVMRImagePresenterConfig9::GetRenderingPrefs, IVMRImagePresenterConfig9GetRenderingPrefs, dshow.ivmrimagepresenterconfig9_getrenderingprefs, vmr9/IVMRImagePresenterConfig9::GetRenderingPrefs
ms.topic: method
f1_keywords: ["vmr9/IVMRImagePresenterConfig9.GetRenderingPrefs"]
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
 - IVMRImagePresenterConfig9.GetRenderingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImagePresenterConfig9::GetRenderingPrefs


## -description



The <code>GetRenderingPrefs</code> method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.



The VMR-9 filter's <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getrenderingprefs">IVMRFilterConfig9::GetRenderingPrefs</a> method calls through to this method.


## -parameters




### -param dwRenderFlags [out]

Receives a bitwise OR of flag from the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/ne-vmr9-__midl___midl_itf_vmr9_0000_0008_0001">VMR9RenderPrefs</a> enumeration, indicating the current rendering settings on the allocator-presenter.


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
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9">IVMRImagePresenterConfig9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

