---
UID: NF:oleauto.VarSub
title: VarSub function (oleauto.h)
author: windows-sdk-content
description: Subtracts two variants.
old-location: automat\varsub.htm
tech.root: automat
ms.assetid: 395cc5fe-8694-47a9-8e92-1768c300ba7e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VarSub, VarSub function [Automation], _oa96_VarSub, automat.varsub, oleauto/VarSub
ms.topic: function
f1_keywords: ["oleauto/VarSub"]
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
 - VarSub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarSub function


## -description


Subtracts two variants.


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
<td>Both expressions are strings</td>
<td>Subtraction</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Subtraction</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Subtraction</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Subtraction</td>
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
 



