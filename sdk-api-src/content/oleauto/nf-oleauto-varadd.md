---
UID: NF:oleauto.VarAdd
title: VarAdd function
author: windows-sdk-content
description: Returns the sum of two variants.
old-location: automat\varadd.htm
old-project: automat
ms.assetid: bdec33b1-cbdd-4ec3-83b2-4e5655ecf5bb
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: VarAdd, VarAdd function [Automation], _oa96_VarAdd, automat.varadd, oleauto/VarAdd
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarAdd
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarAdd function


## -description


Returns the sum of two variants.


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
<td>Concatenated</td>
</tr>
<tr>
<td>One expression is a string and the other a character</td>
<td>Addition</td>
</tr>
<tr>
<td>One expression is numeric and the other a string</td>
<td>Addition</td>
</tr>
<tr>
<td>Both expressions are numeric</td>
<td>Addition</td>
</tr>
<tr>
<td>Either expression is null</td>
<td>Null</td>
</tr>
<tr>
<td>Both expressions are empty</td>
<td>Integer</td>
</tr>
</table>
 



