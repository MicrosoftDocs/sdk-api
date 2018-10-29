---
UID: NF:oleauto.SysReAllocStringLen
title: SysReAllocStringLen function
author: windows-sdk-content
description: Creates a new BSTR containing a specified number of characters from an old BSTR, and frees the old BSTR.
old-location: automat\sysreallocstringlen.htm
tech.root: automat
ms.assetid: d134cff1-7cc8-4284-a216-3819615e3017
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SysReAllocStringLen, SysReAllocStringLen function [Automation], _oa96_SysReAllocStringLen, automat.sysreallocstringlen, oleauto/SysReAllocStringLen
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
 - SysReAllocStringLen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SysReAllocStringLen function


## -description


Creates a new BSTR containing a specified number of characters from an old BSTR, and frees the old BSTR.


## -parameters




### -param pbstr [in, out]

The previously allocated string.


### -param psz [in, optional]

The string from which to copy <i>len</i> characters, or NULL to keep the string uninitialized.


### -param len [in]

The number of characters to copy. A null character is placed afterward, allocating a total of <i>len</i> plus one characters.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The string is reallocated successfully.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists.

</td>
</tr>
</table>
 




## -remarks



Allocates a new string, copies <i>len</i> characters from the passed string into it, and then appends a null character. Frees the BSTR referenced currently by <i>pbstr</i>, and resets <i>pbstr</i> to point to the new BSTR. If <i>psz</i> is null, a string of length <i>len</i> is allocated but not initialized.

The <i>psz</i> string can contain embedded null characters and does not need to end with a null.

If this function is passed a NULL pointer, there will be an access violation and the program will crash. It is your responsibility to protect this function against NULL pointers.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

