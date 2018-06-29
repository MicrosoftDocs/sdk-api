---
UID: NF:evalcom2.IValidate.SetStatus
title: IValidate::SetStatus
author: windows-sdk-content
description: The SetStatus method enables an authoring tool to receive information about the progress of validation through a registered callback function.
old-location: setup\ivalidate_setstatus.htm
old-project: Msi
ms.assetid: 523334f1-4a82-4981-9c77-fffd2b5b561e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IValidate interface,SetStatus method, IValidate.SetStatus, IValidate::SetStatus, SetStatus, SetStatus method, SetStatus method,IValidate interface, evalcom2/IValidate::SetStatus, setup.ivalidate_setstatus
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
 - IValidate.SetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IValidate::SetStatus


## -description


The <b>SetStatus</b> method enables an authoring tool to receive information about the progress of validation through a registered callback function.


## -parameters




### -param pStatusFunction [in]

Specifies a callback function that conforms to the <a href="https://msdn.microsoft.com/76504031-b63a-40fc-aa5b-728f3551057b">LPEVALCOMCALLBACK</a> specification.  The <i>pStatusFunction</i> can be <b>NULL</b>.


### -param pContext

A pointer to an application context that is passed to the callback function. This parameter can be used for error checking.  The <i>pContext</i> can be <b>NULL</b>.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

