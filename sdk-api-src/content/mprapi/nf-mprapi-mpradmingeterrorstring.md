---
UID: NF:mprapi.MprAdminGetErrorString
title: MprAdminGetErrorString function
author: windows-sdk-content
description: The MprAdminGetErrorString function returns the string associated with a router error from Mprerror.h.
old-location: rras\mpradmingeterrorstring.htm
tech.root: rras
ms.assetid: d086f12e-7352-4a0d-bfbe-ddab3b44d757
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: MprAdminGetErrorString, MprAdminGetErrorString function [RAS], _mpr_mpradmingeterrorstring, mprapi/MprAdminGetErrorString, rras.mpradmingeterrorstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminGetErrorString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminGetErrorString function


## -description


The 
<b>MprAdminGetErrorString</b> function returns the string associated with a router error from Mprerror.h.


## -parameters




### -param dwError [in]

Specifies the error code for a  router error.


### -param lplpwsErrorString [out]

Pointer to an <b>LPWSTR</b> variable that points to the text associated with the <i>dwError</i> code on successful return. Free this memory by calling 
<a href="https://msdn.microsoft.com/en-us/library/Aa366730(v=VS.85).aspx">LocalFree</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MR_MID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The error code in <i>dwError</i> is unknown.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa366730(v=VS.85).aspx">LocalFree</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

