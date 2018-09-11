---
UID: NF:strmif.IVMRDeinterlaceControl.GetDeinterlacePrefs
title: IVMRDeinterlaceControl::GetDeinterlacePrefs
author: windows-sdk-content
description: The GetDeinterlacePrefs method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.
old-location: dshow\ivmrdeinterlacecontrol_getdeinterlaceprefs.htm
tech.root: DirectShow
ms.assetid: bb9de83c-087e-4d6e-861a-7db388d59a7c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetDeinterlacePrefs, GetDeinterlacePrefs method [DirectShow], GetDeinterlacePrefs method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetDeinterlacePrefs method, IVMRDeinterlaceControl.GetDeinterlacePrefs, IVMRDeinterlaceControl::GetDeinterlacePrefs, IVMRDeinterlaceControlGetDeinterlacePrefs, dshow.ivmrdeinterlacecontrol_getdeinterlaceprefs, strmif/IVMRDeinterlaceControl::GetDeinterlacePrefs
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
 - IVMRDeinterlaceControl.GetDeinterlacePrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRDeinterlaceControl::GetDeinterlacePrefs


## -description


The <b>GetDeinterlacePrefs</b> method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.


## -parameters




### -param lpdwDeinterlacePrefs [in]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/3f88abac-fc57-4f31-9a4c-cf0f7317d6f8">VMRDeinterlacePrefs</a> enumeration.


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
 




## -remarks



By default, the preferred deinterlacing mode is the first mode reported by the driver. The application can set the preferred mode by calling the <a href="https://msdn.microsoft.com/1a716e10-5382-4b2b-9a4b-b3998a584956">IVMRDeinterlaceControl::SetDeinterlaceMode</a> method. If the VMR cannot use the preferred mode, it will fall back to another mode as specified by the <i>dwDeinterlacePrefs</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>



<a href="https://msdn.microsoft.com/5a78b8cc-ecf8-4e0a-87f0-56b7aac6abdd">IVMRDeinterlaceControl::SetDeinterlacePrefs</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

