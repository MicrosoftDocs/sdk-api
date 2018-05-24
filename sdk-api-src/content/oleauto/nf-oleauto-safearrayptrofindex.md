---
UID: NF:oleauto.SafeArrayPtrOfIndex
title: SafeArrayPtrOfIndex function
author: windows-driver-content
description: Gets a pointer to an array element.
old-location: automat\safearrayptrofindex.htm
old-project: automat
ms.assetid: a73cfd50-89b5-4025-817c-e6c06cc0b300
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: SafeArrayPtrOfIndex, SafeArrayPtrOfIndex function [Automation], _oa96_SafeArrayPtrOfIndex, automat.safearrayptrofindex, oleauto/SafeArrayPtrOfIndex
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
-	SafeArrayPtrOfIndex
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SafeArrayPtrOfIndex function


## -description


Gets a pointer to an array element.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param rgIndices [in]

An array of index values that identify an element of the array. All indexes for the element must be specified.


### -param ppvData [out]

The array element.


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
The specified index is not valid.

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
 




## -remarks



The array should be locked before <b>SafeArrayPtrOfIndex</b> is called. Failing to lock the array can cause unpredictable results.



