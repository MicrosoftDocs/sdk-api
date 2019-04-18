---
UID: NF:oleauto.SafeArrayUnlock
title: SafeArrayUnlock function (oleauto.h)
author: windows-sdk-content
description: Decrements the lock count of an array so it can be freed or resized.
old-location: automat\safearrayunlock.htm
tech.root: automat
ms.assetid: 654995ab-1959-44dc-9e26-11c34e489c14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SafeArrayUnlock, SafeArrayUnlock function [Automation], _oa96_SafeArrayUnlock, automat.safearrayunlock, oleauto/SafeArrayUnlock
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
 - SafeArrayUnlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SafeArrayUnlock function


## -description


Decrements the lock count of an array so it can be freed or resized.


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
 




## -remarks



This function is called after access to the data in an array is finished.


#### Thread Safety

All public static members of the <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY data type</a> are thread safe. Instance members are not guaranteed to be thread safe.

For example, consider an application that uses the <a href="https://msdn.microsoft.com/cb29d862-c7c5-4852-b017-c29e88d5f1c4">SafeArrayLock</a> and SafeArrayUnlock functions. If these functions are called concurrently from different threads on the same <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY data type</a> instance, an inconsistent lock count may be created. This will eventually cause the SafeArrayUnlock function to return E_UNEXPECTED. You can prevent this by providing your own synchronization code.



