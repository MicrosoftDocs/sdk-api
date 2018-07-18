---
UID: NF:evalcom2.IValidate.Validate
title: IValidate::Validate
author: windows-sdk-content
description: The Validate method performs validation of the installation package or merge module using the specified internal consistency evaluator file.
old-location: setup\ivalidate_validate.htm
old-project: Msi
ms.assetid: f7a50031-52ac-4ea2-847c-6212706a9cbd
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IValidate interface,Validate method, IValidate.Validate, IValidate::Validate, Validate, Validate method, Validate method,IValidate interface, evalcom2/IValidate::Validate, setup.ivalidate_validate
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
 - IValidate.Validate
product: Windows
targetos: Windows
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IValidate::Validate


## -description


The <b>Validate</b> method performs validation of the installation package or merge module using the specified internal consistency evaluator file.


## -parameters




### -param wzICEs






#### - szICEs [in, optional]

Optional parameter that specifies which  <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluators (ICE)</a> should run.  You can specify the ICEs in a delimited list or in a custom table. 

When providing a delimited list of ICEs to be run, separate the ICEs in the list by colons (:), for example, "ICE01:ICE03:ICE08".

When providing the name of a custom sequence table, the ICEs to be run can be entered in the custom table. 

If the value of <i>szICEs</i> is <b>NULL</b>, all ICEs in the _ICESequence table are run. The _ICESequence table is the default table provided with orca.msi and msival2.msi.


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
<dt><b>S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The method failed. 

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
 




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

