---
UID: NF:oleauto.SysReAllocString
title: SysReAllocString function
author: windows-sdk-content
description: Reallocates a previously allocated string to be the size of a second string and copies the second string into the reallocated memory.
old-location: automat\sysreallocstring.htm
old-project: automat
ms.assetid: 0207c33b-c065-42bb-8d70-ccdc3fddb338
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: SysReAllocString, SysReAllocString function [Automation], _oa96_SysReAllocString, automat.sysreallocstring, oleauto/SysReAllocString
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SysReAllocString
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SysReAllocString function


## -description


Reallocates a previously allocated string to be the size of a second string and copies the second string into the reallocated memory.


## -parameters




### -param pbstr [in, out]

The previously allocated string.


### -param psz [in, optional]

The string to copy.


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



The address passed in psz cannot be part of the string passed in pbstr, or unexpected results may occur.

If pbstr is NULL, there will be an access violation and the program will crash. It is your responsibility to protect this function against NULL pointers.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

