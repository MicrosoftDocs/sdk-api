---
UID: NF:evalcom2.IValidate.CloseCUB
title: IValidate::CloseCUB
author: windows-sdk-content
description: The CloseCUB method closes an open Internal Consistency Evaluator (ICE) .cub file. Internal Consistency Evaluator (ICE) .cub files can be opened using the OpenCUB method.
old-location: setup\ivalidate_closecub.htm
old-project: Msi
ms.assetid: be0d21ee-bb15-4c6d-9d69-741adf047863
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CloseCUB, CloseCUB method, CloseCUB method,IValidate interface, IValidate interface,CloseCUB method, IValidate.CloseCUB, IValidate::CloseCUB, evalcom2/IValidate::CloseCUB, setup.ivalidate_closecub
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
tech.root: 
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Evalcom2.dll
api_name:
 - IValidate.CloseCUB
product: Windows
targetos: Windows
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IValidate::CloseCUB


## -description


The <b>CloseCUB</b> method closes an open <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluator (ICE)</a> .cub file. Internal Consistency Evaluator (ICE) .cub files can be opened using the <a href="https://msdn.microsoft.com/cadf3c6e-6fbb-4d46-b9a8-4f2508f1e8bc">OpenCUB</a> method.


## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method failed. 

</td>
</tr>
</table>
 




## -remarks



The method returns S_FALSE if no .cub file has been opened using the <a href="https://msdn.microsoft.com/cadf3c6e-6fbb-4d46-b9a8-4f2508f1e8bc">OpenCUB</a> method.




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

