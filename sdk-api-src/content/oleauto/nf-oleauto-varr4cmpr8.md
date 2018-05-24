---
UID: NF:oleauto.VarR4CmpR8
title: VarR4CmpR8 function
author: windows-driver-content
description: Compares two variants of types float and double.
old-location: automat\varr4cmpr8.htm
old-project: automat
ms.assetid: 0c871779-cfe2-4857-a391-ee28aca6c950
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarR4CmpR8, VarR4CmpR8 function [Automation], _oa96_VarR4CmpR8, automat.varr4cmpr8, oleauto/VarR4CmpR8
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
-	VarR4CmpR8
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VarR4CmpR8 function


## -description


Compares two variants of types float and double.


## -parameters




### -param fltLeft [in]

The first variant.


### -param dblRight [in]

The second variant.


## -returns



The function returns the following as a SUCCESS HRESULT.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>fltLeft</i> is less than <i>dblRight.</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The two parameters are equal.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>fltLeft</i> is greater than <i>dblRight.</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Either expression is NULL.


</td>
</tr>
</table>
 



