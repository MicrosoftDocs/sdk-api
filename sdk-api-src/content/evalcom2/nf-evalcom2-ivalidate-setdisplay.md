---
UID: NF:evalcom2.IValidate.SetDisplay
title: IValidate::SetDisplay (evalcom2.h)
description: The SetDisplay method enables an authoring tool to obtain ICE status messages through a callback function.
helpviewer_keywords: ["IValidate interface","SetDisplay method","IValidate.SetDisplay","IValidate::SetDisplay","SetDisplay","SetDisplay method","SetDisplay method","IValidate interface","evalcom2/IValidate::SetDisplay","setup.ivalidate_setdisplay"]
old-location: setup\ivalidate_setdisplay.htm
tech.root: setup
ms.assetid: e376740e-82fc-44da-b200-c74d73978c6e
ms.date: 12/05/2018
ms.keywords: IValidate interface,SetDisplay method, IValidate.SetDisplay, IValidate::SetDisplay, SetDisplay, SetDisplay method, SetDisplay method,IValidate interface, evalcom2/IValidate::SetDisplay, setup.ivalidate_setdisplay
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValidate::SetDisplay
 - evalcom2/IValidate::SetDisplay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Evalcom2.dll
api_name:
 - IValidate.SetDisplay
---

# IValidate::SetDisplay


## -description

The <b>SetDisplay</b> method enables an authoring tool to obtain ICE status messages through a callback function.

## -parameters

### -param pDisplayFunction [in]

		Specifies a callback function that conforms to the <a href="/windows/desktop/api/evalcom2/nc-evalcom2-lpdisplayval">LPDISPLAYVAL</a> specification.

### -param pContext [in]

A pointer to an application context that is passed to the callback function. This parameter can be used for error checking.  The <i>pContext</i> parameter can be <b>NULL</b>.

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
The <i>pDisplayFunction</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>