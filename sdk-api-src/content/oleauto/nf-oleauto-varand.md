---
UID: NF:oleauto.VarAnd
title: VarAnd function (oleauto.h)
author: windows-sdk-content
description: Performs a bitwise And operation between two variants of any integral type.
old-location: automat\varand.htm
tech.root: automat
ms.assetid: bcdda3e6-d599-4266-ba66-6634ab26f9d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VarAnd, VarAnd function [Automation], _oa96_VarAnd, automat.varand, oleauto/VarAnd
ms.topic: function
f1_keywords: 
 - "oleauto/VarAnd"
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
 - VarAnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarAnd function


## -description


Performs a bitwise And operation between two variants of any integral type.


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
<th><i>pvarLeft</i></th>
<th><i>pvarRight</i></th>
<th><i>pvarResult</i></th>
</tr>
<tr>
<td>TRUE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>TRUE</td>
<td>FALSE</td>
<td>FALSE</td>
</tr>
<tr>
<td>TRUE</td>
<td>NULL</td>
<td>NULL</td>
</tr>
<tr>
<td>FALSE</td>
<td>TRUE</td>
<td>FALSE</td>
</tr>
<tr>
<td>FALSE</td>
<td>FALSE</td>
<td>FALSE</td>
</tr>
<tr>
<td>FALSE</td>
<td>NULL</td>
<td>FALSE</td>
</tr>
<tr>
<td>NULL</td>
<td>TRUE</td>
<td>NULL</td>
</tr>
<tr>
<td>NULL</td>
<td>FALSE</td>
<td>FALSE</td>
</tr>
<tr>
<td>NULL</td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>
 



