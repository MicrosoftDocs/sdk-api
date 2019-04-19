---
UID: NF:oleauto.VarDecCmp
title: VarDecCmp function (oleauto.h)
author: windows-sdk-content
description: Compares two variants of type decimal.
old-location: automat\vardeccmp.htm
tech.root: automat
ms.assetid: ebb418c0-c15d-42c2-88a3-1ffcd36a2750
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VarDecCmp, VarDecCmp function [Automation], _oa96_VarDecCmp, automat.vardeccmp, oleauto/VarDecCmp
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
 - VarDecCmp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarDecCmp function


## -description


Compares two variants of type decimal.


## -parameters




### -param pdecLeft [in]

The first variant.


### -param pdecRight [in]

The second variant.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_LT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>pdecLeft</i> is less than <i>dblRight</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_EQ</b></dt>
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
<dt><b>VARCMP_GT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>pdecLeft</i> is greater than <i>dblRight</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_NULL</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Either expression is null.

</td>
</tr>
</table>
 



