---
UID: NF:bcrypt.BCryptSetProperty
title: BCryptSetProperty function (bcrypt.h)
description: Sets the value of a named property for a CNG object.
helpviewer_keywords: ["BCryptSetProperty","BCryptSetProperty function [Security]","bcrypt/BCryptSetProperty","security.bcryptsetproperty_func"]
old-location: security\bcryptsetproperty_func.htm
tech.root: security
ms.assetid: 687f3410-d28b-4ce2-a2a1-c564f757c668
ms.date: 12/05/2018
ms.keywords: BCryptSetProperty, BCryptSetProperty function [Security], bcrypt/BCryptSetProperty, security.bcryptsetproperty_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptSetProperty
 - bcrypt/BCryptSetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptSetProperty
---

# BCryptSetProperty function


## -description

The <b>BCryptSetProperty</b> function sets the value of a named property for a CNG object.

## -parameters

### -param hObject [in, out]

A handle that represents the CNG object to set the property value for.

### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to set. This can be one of the predefined <a href="/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a> or a custom property identifier.

### -param pbInput [in]

The address of a buffer that contains the new property value. The <i>cbInput</i> parameter contains the size of this buffer.

### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hObject</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The named property specified by the <i>pszProperty</i> parameter is not supported or is read-only.

</td>
</tr>
</table>

## -remarks

Depending on what processor modes a provider supports, <b>BCryptSetProperty</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, any pointers passed to <b>BCryptSetProperty</b> must refer to nonpaged (or locked) memory. If the object specified in the <i>hObject</i> parameter is a handle, it must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

When setting the value for the property <i>BCRYPT_CHAINING_MODE</i>, the <i>pbInput</i> parameter is unbounded by <i>cbInput</i>. The caller needs to ensure a valid null-terminated Unicode string is provided.
