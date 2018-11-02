---
UID: NF:oleauto.VarMul
title: VarMul function
author: windows-sdk-content
description: Returns the result from multiplying two variants.
old-location: automat\varmul.htm
tech.root: automat
ms.assetid: d804a23b-7d52-4f11-a93e-3eb02a079d2c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: VarMul, VarMul function [Automation], _oa96_VarMul, automat.varmul, oleauto/VarMul
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarMul
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VarMul function


## -description


Returns the result from multiplying two variants.


## -parameters




### -param pvarLeft [in]

The first variant.


### -param pvarRight [in]

The second variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function operates as follows.

<table>
<tr>
<th>Condition</th>
<th>Result</th>
</tr>
<tr>
<td>Both expressions are strings, dates, characters, or boolean values</td>
<td>Multiplication</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Multiplication</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Multiplication</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Multiplication</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>Empty string</td>
</tr>
</table>
 

Boolean values are converted to -1 for FALSE and 0 for TRUE.



