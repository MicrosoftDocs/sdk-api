---
UID: NF:oleauto.VarNot
title: VarNot function
author: windows-driver-content
description: Performs the bitwise not negation operation on a variant.
old-location: automat\varnot.htm
old-project: automat
ms.assetid: e3825905-2a28-4283-bb65-0273572f3150
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarNot, VarNot function [Automation], _oa96_VarNot, automat.varnot, oleauto/VarNot
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
-	VarNot
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VarNot function


## -description


Performs the bitwise not negation operation on a variant.


## -parameters




### -param pvarIn [in]

The variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function operates as follows.

<table>
<tr>
<th><i>pvarIn</i></th>
<th><i>pvarResult</i></th>
</tr>
<tr>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>FALSE</td>
<td>TRUE</td>
</tr>
<tr>
<td>NULL</td>
<td>NULL</td>
</tr>
</table>
 



