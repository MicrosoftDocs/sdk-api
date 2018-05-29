---
UID: NF:mprapi.MprAdminInterfaceEnum
title: MprAdminInterfaceEnum function
author: windows-sdk-content
description: The MprAdminInterfaceEnum function enumerates all the interfaces on a specified server.
old-location: rras\mpradmininterfaceenum.htm
old-project: RRAS
ms.assetid: 50486ad3-2f1d-4ab9-9a7f-7b72128486fb
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprAdminInterfaceEnum, MprAdminInterfaceEnum function [RAS], _mpr_mpradmininterfaceenum, mprapi/MprAdminInterfaceEnum, rras.mpradmininterfaceenum
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminInterfaceEnum
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminInterfaceEnum function


## -description


The 
<b>MprAdminInterfaceEnum</b> function enumerates all the interfaces on a specified server.


## -parameters




### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.


### -param lplpbBuffer [out]

On successful completion, a pointer to an array of <a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a> structures.  Free this memory buffer by calling 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


### -param dwPrefMaxLen [in]

Specifies the preferred maximum length of returned data (in 8-bit bytes). If this parameter is -1, the buffer returned is large enough to hold all available information.


### -param lpdwEntriesRead [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of interfaces that were enumerated from the current position in the enumeration.


### -param lpdwTotalEntries [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of interfaces that could have been enumerated from the current resume position.


### -param lpdwResumeHandle [in]

Pointer to a <b>DWORD</b> variable. This variable specifies a resume handle that can be used to continue the enumeration. The handle should be zero on the first call, and left unchanged on subsequent calls. If the return code is ERROR_MORE_DATA then the call can be re-issued using the handle to retrieve more data. If on return, the handle is <b>NULL</b>, the enumeration cannot be continued. For other types of error returns, this handle is invalid. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return a resume handle.


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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More information is available; the enumeration can be continued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwLevel</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>



<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

