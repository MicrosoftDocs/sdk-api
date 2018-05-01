---
UID: NF:oleauto.SafeArrayGetLBound
title: SafeArrayGetLBound function
author: windows-driver-content
description: Gets the lower bound for any dimension of the specified safe array.
old-location: automat\safearraygetlbound.htm
old-project: automat
ms.assetid: f3134cc9-759b-4908-ada0-d025a525e795
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: SafeArrayGetLBound, SafeArrayGetLBound function [Automation], _oa96_SafeArrayGetLBound, automat.safearraygetlbound, oleauto/SafeArrayGetLBound
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
-	SafeArrayGetLBound
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SafeArrayGetLBound function


## -description


Gets the lower bound for any dimension of the specified safe array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


### -param nDim [in]

The array dimension for which to get the lower bound.


### -param plLbound [out]

The lower bound.


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
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified index is out of bounds.

</td>
</tr>
</table>
 



