---
UID: NC:evalcom2.LPDISPLAYVAL
title: LPDISPLAYVAL
author: windows-sdk-content
description: The LPDISPLAYVAL function specification defines a callback function prototype. The IValidate::SetDisplay method enables an authoring tool to receive ICE status messages through the registered callback function.
old-location: setup\lpdisplayval.htm
old-project: msi
ms.assetid: ff7b2789-a825-4fa4-b00c-a538f37d0eba
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LPDISPLAYVAL, LPDISPLAYVAL callback, LPDISPLAYVAL callback function, evalcom2/LPDISPLAYVAL, ieError, ieInfo, ieUnknown, ieWarning, setup.lpdisplayval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: evalcom2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evalcom2.h
api_name:
 - LPDISPLAYVAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# LPDISPLAYVAL callback function


## -description


The <b>LPDISPLAYVAL</b> function specification defines a callback function prototype. The <a href="https://msdn.microsoft.com/e376740e-82fc-44da-b200-c74d73978c6e">IValidate::SetDisplay</a> method enables an authoring tool to receive ICE status messages through the registered callback function.


## -parameters




### -param pContext

A pointer to an application context passed to the <a href="https://msdn.microsoft.com/e376740e-82fc-44da-b200-c74d73978c6e">SetDisplay</a> method. 

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
<dt><b><b>TRUE</b></b></dt>
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
<dt><b><b>FALSE</b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Validation was canceled. The callback function return <b>FALSE</b> to stop validation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

