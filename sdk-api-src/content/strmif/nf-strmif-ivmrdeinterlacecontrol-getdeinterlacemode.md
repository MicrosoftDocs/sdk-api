---
UID: NF:strmif.IVMRDeinterlaceControl.GetDeinterlaceMode
title: IVMRDeinterlaceControl::GetDeinterlaceMode
author: windows-sdk-content
description: The GetDeinterlaceMode method retrieves the deinterlacing mode for the specified video stream.
old-location: dshow\ivmrdeinterlacecontrol_getdeinterlacemode.htm
tech.root: DirectShow
ms.assetid: 558b4902-596a-45f9-ad95-f8e868ba4a30
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeinterlaceMode, GetDeinterlaceMode method [DirectShow], GetDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetDeinterlaceMode method, IVMRDeinterlaceControl.GetDeinterlaceMode, IVMRDeinterlaceControl::GetDeinterlaceMode, IVMRDeinterlaceControlGetDeinterlaceMode, dshow.ivmrdeinterlacecontrol_getdeinterlacemode, strmif/IVMRDeinterlaceControl::GetDeinterlaceMode
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
 - IVMRDeinterlaceControl.GetDeinterlaceMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRDeinterlaceControl::GetDeinterlaceMode


## -description


The <b>GetDeinterlaceMode</b> method retrieves the deinterlacing mode for the specified video stream.


## -parameters




### -param dwStreamID [in]

Index of the video stream to check.


### -param lpDeinterlaceMode [out]

Pointer to a variable that receives a GUID. The GUID identifies the deinterlacing mode currently in use. If no deinterlacing mode was set, the value is GUID_NULL.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No deinterlacing mode was set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>
 




## -remarks



The VMR may not be able to use the requested mode, in which case it falls back to another deinterlace mode, as specified in the <a href="https://msdn.microsoft.com/5a78b8cc-ecf8-4e0a-87f0-56b7aac6abdd">IVMRDeinterlaceControl::SetDeinterlacePrefs</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>



<a href="https://msdn.microsoft.com/1a716e10-5382-4b2b-9a4b-b3998a584956">IVMRDeinterlaceControl::SetDeinterlaceMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

