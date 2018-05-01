---
UID: NF:oleauto.SafeArrayUnaccessData
title: SafeArrayUnaccessData function
author: windows-driver-content
description: Decrements the lock count of an array, and invalidates the pointer retrieved by SafeArrayAccessData.
old-location: automat\safearrayunaccessdata.htm
old-project: automat
ms.assetid: 61b482cb-f0a3-4efb-9a68-f373f241e89a
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: SafeArrayUnaccessData, SafeArrayUnaccessData function [Automation], _oa96_SafeArrayUnaccessData, automat.safearrayunaccessdata, oleauto/SafeArrayUnaccessData
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
-	SafeArrayUnaccessData
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SafeArrayUnaccessData function


## -description


Decrements the lock count of an array, and invalidates the pointer retrieved by <a href="https://msdn.microsoft.com/ded2112e-f6cd-4982-bacb-b95370e80187">SafeArrayAccessData</a>.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


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
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be unlocked.

</td>
</tr>
</table>
 



