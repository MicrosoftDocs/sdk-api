---
UID: NF:oleauto.SafeArrayGetUBound
title: SafeArrayGetUBound function (oleauto.h)
author: windows-sdk-content
description: Gets the upper bound for any dimension of the specified safe array.
old-location: automat\safearraygetubound.htm
tech.root: automat
ms.assetid: aed339d5-d962-4adc-ac01-6c15a54c51ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SafeArrayGetUBound, SafeArrayGetUBound function [Automation], _oa96_SafeArrayGetUBound, automat.safearraygetubound, oleauto/SafeArrayGetUBound
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
 - SafeArrayGetUBound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayGetUBound function


## -description


Gets the upper bound for any dimension of the specified safe array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


### -param nDim [in]

The array dimension for which to get the upper bound.




### -param plUbound [out]

The upper bound.


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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified index is out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Overflow occurred while computing the upper bound.

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
</table>
 



