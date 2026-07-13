---
UID: NC:evalcom2.LPDISPLAYVAL
title: LPDISPLAYVAL (evalcom2.h)
description: The LPDISPLAYVAL function specification defines a callback function prototype. The IValidate::SetDisplay method enables an authoring tool to receive ICE status messages through the registered callback function.
helpviewer_keywords: ["LPDISPLAYVAL","LPDISPLAYVAL callback","LPDISPLAYVAL callback function","evalcom2/LPDISPLAYVAL","ieError","ieInfo","ieUnknown","ieWarning","setup.lpdisplayval"]
old-location: setup\lpdisplayval.htm
tech.root: setup
ms.assetid: ff7b2789-a825-4fa4-b00c-a538f37d0eba
ms.date: 12/05/2018
ms.keywords: LPDISPLAYVAL, LPDISPLAYVAL callback, LPDISPLAYVAL callback function, evalcom2/LPDISPLAYVAL, ieError, ieInfo, ieUnknown, ieWarning, setup.lpdisplayval
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDISPLAYVAL
 - evalcom2/LPDISPLAYVAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evalcom2.h
api_name:
 - LPDISPLAYVAL
---

# LPDISPLAYVAL callback function


## -description

The <b>LPDISPLAYVAL</b> function specification defines a callback function prototype. The <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay">IValidate::SetDisplay</a> method enables an authoring tool to receive ICE status messages through the registered callback function.

## -parameters

### -param pContext

A pointer to an application context passed to the <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay">SetDisplay</a> method. 

This parameter can be used for error checking.

### -param uiType [in]

Specifies the type of message sent by the ICE. 

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ieUnknown"></a><a id="ieunknown"></a><a id="IEUNKNOWN"></a><dl>
<dt><b>ieUnknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unknown ICE message.

</td>
</tr>
<tr>
<td width="40%"><a id="ieError"></a><a id="ieerror"></a><a id="IEERROR"></a><dl>
<dt><b>ieError</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
ICE error message.

</td>
</tr>
<tr>
<td width="40%"><a id="ieWarning"></a><a id="iewarning"></a><a id="IEWARNING"></a><dl>
<dt><b>ieWarning</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
ICE warning message.

</td>
</tr>
<tr>
<td width="40%"><a id="ieInfo"></a><a id="ieinfo"></a><a id="IEINFO"></a><dl>
<dt><b>ieInfo</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
ICE information message.

</td>
</tr>
</table>

### -param szwVal [in]

The name of the ICE reporting the message, or an error reported by evalcom2 during validation.

### -param szwDescription [in]

The message text.

### -param szwLocation [in]

The location of the error. 

This parameter can be <b>NULL</b> if the error does not refer to an actual database table or row. Specify the location of the error using the following format: Table\tColumn\tPrimaryKey1[\tPrimaryKey2\ . . .].

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Validation procedure should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Validation was canceled. The callback function return <b>FALSE</b> to stop validation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>