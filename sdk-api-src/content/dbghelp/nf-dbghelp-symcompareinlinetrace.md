---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# SymCompareInlineTrace function


## -description


Compares two inline traces.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Address1 [in]

The first address to be compared.


### -param InlineContext1 [in]

The inline context for the first trace to be compared.


### -param RetAddress1 [in]

The return address of the first trace to be compared.


### -param Address2 [in]

The second address to be compared.


### -param RetAddress2 [in]

The return address of the second trace to be compared.


## -returns



Indicates the result of the comparison.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_ERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_IDENTICAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The inline contexts are identical.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPIN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-in of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPOUT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-out of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_STEPOVER</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The inline trace is a step-over of an inline function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYM_INLINE_COMP_DIFFERENT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The inline contexts are different.

</td>
</tr>
</table>
 



