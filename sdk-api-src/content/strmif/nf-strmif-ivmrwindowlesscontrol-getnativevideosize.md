---
UID: NF:strmif.IVMRWindowlessControl.GetNativeVideoSize
title: IVMRWindowlessControl::GetNativeVideoSize (strmif.h)
description: The GetNativeVideoSize method retrieves the un-stretched video size and aspect ratio of the video.
helpviewer_keywords: ["GetNativeVideoSize","GetNativeVideoSize method [DirectShow]","GetNativeVideoSize method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetNativeVideoSize method","IVMRWindowlessControl.GetNativeVideoSize","IVMRWindowlessControl::GetNativeVideoSize","IVMRWindowlessControlGetNativeVideoSize","dshow.ivmrwindowlesscontrol_getnativevideosize","strmif/IVMRWindowlessControl::GetNativeVideoSize"]
old-location: dshow\ivmrwindowlesscontrol_getnativevideosize.htm
tech.root: dshow
ms.assetid: cc8fd96d-e9a8-4911-9330-a4cf71a2d926
ms.date: 12/05/2018
ms.keywords: GetNativeVideoSize, GetNativeVideoSize method [DirectShow], GetNativeVideoSize method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetNativeVideoSize method, IVMRWindowlessControl.GetNativeVideoSize, IVMRWindowlessControl::GetNativeVideoSize, IVMRWindowlessControlGetNativeVideoSize, dshow.ivmrwindowlesscontrol_getnativevideosize, strmif/IVMRWindowlessControl::GetNativeVideoSize
f1_keywords:
- strmif/IVMRWindowlessControl.GetNativeVideoSize
dev_langs:
- c++
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
- IVMRWindowlessControl.GetNativeVideoSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::GetNativeVideoSize


## -description



The <code>GetNativeVideoSize</code> method retrieves the un-stretched video size and aspect ratio of the video.




## -parameters




### -param lpWidth [out]

Pointer that receives the width of the native video rectangle.


### -param lpHeight [out]

Pointer that receives the height of the native video rectangle.


### -param lpARWidth [out]

Pointer that receives the aspect ratio width of the native video rectangle.


### -param lpARHeight [out]

Pointer that receives the aspect ratio height of the native video rectangle.


## -returns



If the method succeeds, it returns S_OK. Returns E_POINTER if all four input parameters are <b>NULL</b>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -remarks



If the VMR is not connected to an upstream filter, this method will succeed but all parameters will be set to zero.

If <i>lpWidth</i> is 640 and <i>lpHeight</i> is 480, then <i>lpARWidth</i> will be 4 and <i>lpARHeight</i> will be 3.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

