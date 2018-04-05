---
UID: NF:strmif.IVMRDeinterlaceControl.GetActualDeinterlaceMode
title: IVMRDeinterlaceControl::GetActualDeinterlaceMode method
author: windows-driver-content
description: The GetActualDeinterlaceMode method returns the deinterlacing mode that the VMR is using for a specified stream.
old-location: dshow\ivmrdeinterlacecontrol_getactualdeinterlacemode.htm
old-project: DirectShow
ms.assetid: b8b5c619-68fe-40a5-8621-ef6e9ad612d8
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetActualDeinterlaceMode method [DirectShow], GetActualDeinterlaceMode method [DirectShow], IVMRDeinterlaceControl interface, GetActualDeinterlaceMode,IVMRDeinterlaceControl.GetActualDeinterlaceMode, IVMRDeinterlaceControl, IVMRDeinterlaceControl interface [DirectShow], GetActualDeinterlaceMode method, IVMRDeinterlaceControl::GetActualDeinterlaceMode, IVMRDeinterlaceControlGetActualDeinterlaceMode, dshow.ivmrdeinterlacecontrol_getactualdeinterlacemode, strmif/IVMRDeinterlaceControl::GetActualDeinterlaceMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRDeinterlaceControl.GetActualDeinterlaceMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRDeinterlaceControl::GetActualDeinterlaceMode method


## -description


The <b>GetActualDeinterlaceMode</b> method returns the deinterlacing mode that the VMR is using for a specified stream.


## -parameters




### -param dwStreamID [in]

Index of the video stream.


### -param lpDeinterlaceMode [out]

Pointer to a variable that receives a GUID value that identifies the deinterlacing mode. The method returns GUID_NULL if the VMR has not initialized the deinterlacing hardware, or if the VMR determines that this stream should not be deinterlaced.


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

