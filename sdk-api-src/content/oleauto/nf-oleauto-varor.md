---
UID: NF:oleauto.VarOr
title: VarOr function
author: windows-driver-content
description: Performs a logical disjunction on two variants.
old-location: automat\varor.htm
old-project: automat
ms.assetid: 8c161755-4fdd-48bd-9dc4-6510cc9ce8ab
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarOr, VarOr function [Automation], _oa96_VarOr, automat.varor, oleauto/VarOr
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	VarOr
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VarOr function


## -description


Performs a logical disjunction on two variants.




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
<td>TRUE</td>
</tr>
<tr>
<td>TRUE</td>
<td>NULL</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>FALSE</td>
<td>FALSE</td>
</tr>
<tr>
<td>FALSE</td>
<td>NULL</td>
<td>NULL</td>
</tr>
<tr>
<td>NULL</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>NULL</td>
<td>FALSE</td>
<td>NULL</td>
</tr>
<tr>
<td>NULL</td>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>
 



