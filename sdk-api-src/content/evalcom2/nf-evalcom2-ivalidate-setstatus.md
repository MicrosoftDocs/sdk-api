---
UID: NF:evalcom2.IValidate.SetStatus
title: IValidate::SetStatus (evalcom2.h)
description: The SetStatus method enables an authoring tool to receive information about the progress of validation through a registered callback function.
helpviewer_keywords: ["IValidate interface","SetStatus method","IValidate.SetStatus","IValidate::SetStatus","SetStatus","SetStatus method","SetStatus method","IValidate interface","evalcom2/IValidate::SetStatus","setup.ivalidate_setstatus"]
old-location: setup\ivalidate_setstatus.htm
tech.root: setup
ms.assetid: 523334f1-4a82-4981-9c77-fffd2b5b561e
ms.date: 12/05/2018
ms.keywords: IValidate interface,SetStatus method, IValidate.SetStatus, IValidate::SetStatus, SetStatus, SetStatus method, SetStatus method,IValidate interface, evalcom2/IValidate::SetStatus, setup.ivalidate_setstatus
f1_keywords:
- evalcom2/IValidate.SetStatus
dev_langs:
- c++
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
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Evalcom2.dll
api_name:
- IValidate.SetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IValidate::SetStatus


## -description


The <b>SetStatus</b> method enables an authoring tool to receive information about the progress of validation through a registered callback function.


## -parameters




### -param pStatusFunction [in]

Specifies a callback function that conforms to the <a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nc-evalcom2-lpevalcomcallback">LPEVALCOMCALLBACK</a> specification.  The <i>pStatusFunction</i> can be <b>NULL</b>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>
 

 

