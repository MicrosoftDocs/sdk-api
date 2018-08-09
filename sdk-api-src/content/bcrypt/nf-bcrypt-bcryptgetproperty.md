---
UID: NF:bcrypt.BCryptGetProperty
title: BCryptGetProperty function
author: windows-sdk-content
description: Retrieves the value of a named property for a CNG object.
old-location: security\bcryptgetproperty_func.htm
old-project: seccng
ms.assetid: 5c62ca3a-843e-41a7-9340-41785fbb15f4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BCryptGetProperty, BCryptGetProperty function [Security], bcrypt/BCryptGetProperty, security.bcryptgetproperty_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: HASHALGORITHM_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptGetProperty
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptGetProperty function


## -description


The <b>BCryptGetProperty</b> function retrieves the value of a named property for a CNG object.


## -parameters




### -param hObject [in]

A handle that represents the CNG object to obtain the property value for.


### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to retrieve. This can be one of the predefined <a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">Cryptography Primitive Property Identifiers</a> or a custom property identifier.


### -param pbOutput [out]

The address of a buffer that receives the property value. The <i>cbOutput</i> parameter contains the size of this buffer.


### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer.


### -param pcbResult [out]

A pointer to a <b>ULONG</b> variable that receives the number of bytes that were copied to the <i>pbOutput</i> buffer. If the <i>pbOutput</i> parameter is <b>NULL</b>, this function will place the required size, in bytes, in the location pointed to by this parameter.


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
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified by the <i>cbOutput</i> parameter is not large enough to hold the property value.

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
The named property specified by the <i>pszProperty</i> parameter is not supported.

</td>
</tr>
</table>
 




## -remarks



To obtain the required size for a property, pass <b>NULL</b> for the <i>pbOutput</i> parameter. This function will place the required size, in bytes, in the value pointed to by the <i>pcbResult</i> parameter.

Depending on what processor modes a provider supports, <b>BCryptGetProperty</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, any pointers passed to the <b>BCryptGetProperty</b> function must refer to nonpaged (or locked) memory. If the object specified in the <i>hObject</i> parameter is a handle, it must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.





