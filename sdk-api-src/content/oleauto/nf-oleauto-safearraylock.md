---
UID: NF:oleauto.SafeArrayLock
title: SafeArrayLock function (oleauto.h)
description: Increments the lock count of an array, and places a pointer to the array data in pvData of the array descriptor.
helpviewer_keywords: ["SafeArrayLock","SafeArrayLock function [Automation]","_oa96_SafeArrayLock","automat.safearraylock","oleauto/SafeArrayLock"]
old-location: automat\safearraylock.htm
tech.root: automat
ms.assetid: cb29d862-c7c5-4852-b017-c29e88d5f1c4
ms.date: 12/05/2018
ms.keywords: SafeArrayLock, SafeArrayLock function [Automation], _oa96_SafeArrayLock, automat.safearraylock, oleauto/SafeArrayLock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayLock
 - oleauto/SafeArrayLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayLock
---

# SafeArrayLock function


## -description

Increments the lock count of an array, and places a pointer to the array data in pvData of the array descriptor.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

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
The array could not be locked.

</td>
</tr>
</table>

## -remarks

The pointer in the array descriptor is valid until the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayunlock">SafeArrayUnlock</a> function is called. Calls to <b>SafeArrayLock</b> can be nested, in which case an equal number of calls to <b>SafeArrayUnlock</b> are required.

An array cannot be deleted while it is locked.


#### Thread Safety

All public static (Shared in Visual Basic) members of the <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY data type</a> are thread safe. Instance members are not guaranteed to be thread safe.

For example, consider an application that uses the SafeArrayLock and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayunlock">SafeArrayUnlock</a> functions. If these functions are called concurrently from different threads on the same <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY data type</a> instance, an inconsistent lock count may be created. This will eventually cause the <b>SafeArrayUnlock</b> function to return E_UNEXPECTED. You can prevent this by providing your own synchronization code.