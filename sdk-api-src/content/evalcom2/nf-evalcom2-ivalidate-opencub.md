---
UID: NF:evalcom2.IValidate.OpenCUB
title: IValidate::OpenCUB
author: windows-sdk-content
description: The OpenCUB method opens an Internal Consistency Evaluator (ICE) file that is to be used for validation.
old-location: setup\ivalidate_opencub.htm
old-project: Msi
ms.assetid: cadf3c6e-6fbb-4d46-b9a8-4f2508f1e8bc
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IValidate interface,OpenCUB method, IValidate.OpenCUB, IValidate::OpenCUB, OpenCUB, OpenCUB method, OpenCUB method,IValidate interface, evalcom2/IValidate::OpenCUB, setup.ivalidate_opencub
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Evalcom2.dll
api_name:
-	IValidate.OpenCUB
product: Windows
targetos: Windows
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IValidate::OpenCUB


## -description


The <b>OpenCUB</b> method opens an  <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluator (ICE)</a> file that is to be used for validation.  


## -parameters




### -param szCUBFile [in]

The fully qualified path to the <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluator (ICE)</a> file to be used for validation.


## -returns



This method can return one of these values.

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
The value of <i>szDatabase</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluator (ICE)</a> file typically has a .cub file name extension.




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

