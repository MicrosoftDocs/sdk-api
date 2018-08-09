---
UID: NF:recapis.SetCACMode
title: SetCACMode function
author: windows-sdk-content
description: Specifies character Autocomplete mode for character or word recognition.You cannot turn off character Autocomplete after it is set.
old-location: tablet\setcacmode.htm
old-project: tablet
ms.assetid: 4f51e2e1-612a-484e-acba-6f3ae268082a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 4f51e2e1-612a-484e-acba-6f3ae268082a, CAC_FULL, CAC_PREFIX, CAC_RANDOM, SetCACMode, SetCACMode function [Tablet PC], recapis/SetCACMode, tablet.setcacmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - SetCACMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# SetCACMode function


## -description



Specifies character Autocomplete mode for character or word recognition.

You cannot turn off character Autocomplete after it is set.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param iMode


The following table lists the possible character Autocomplete modes.



<table>
<tr>
<th>The haracter Autocomplete mode.</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAC_FULL"></a><a id="cac_full"></a><dl>
<dt><b>CAC_FULL</b></dt>
</dl>
</td>
<td width="60%">
Recognition occurs as if all strokes have been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="CAC_PREFIX"></a><a id="cac_prefix"></a><dl>
<dt><b>CAC_PREFIX</b></dt>
</dl>
</td>
<td width="60%">
Recognition occurs on partial input. The order of the strokes must conform to the rules of the language.

</td>
</tr>
<tr>
<td width="40%"><a id="CAC_RANDOM"></a><a id="cac_random"></a><dl>
<dt><b>CAC_RANDOM</b></dt>
</dl>
</td>
<td width="60%">
Recognition occurs on partial input. The order of the strokes can be arbitrary.

</td>
</tr>
</table>
 


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified mode is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Either you have not called the <a href="https://msdn.microsoft.com/3ca3c743-83f9-46b0-851a-cba6e4ed980a">SetGuide</a> function before calling this function, or the guide has more than one box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The context is invalid or one of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_OUT_OF_ORDER_CALL</b></dt>
</dl>
</td>
<td width="60%">
Attempted to set guide when there was already some ink in the reco context, or, in the case of recognizers of East Asian characters, <a href="https://msdn.microsoft.com/3ca3c743-83f9-46b0-851a-cba6e4ed980a">SetGuide</a> was called previously.

</td>
</tr>
</table>
 



