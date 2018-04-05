---
UID: NF:mprapi.MprAdminPortEnum
title: MprAdminPortEnum function
author: windows-driver-content
description: Enumerates all active ports in a specific connection, or all ports available for use or currently used by RAS.
old-location: rras\mpradminportenum.htm
old-project: RRAS
ms.assetid: b6caa1f0-f4c7-48a9-b1e8-b484e7d7a3a3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: MprAdminPortEnum, MprAdminPortEnum function [RAS], _mpr_mpradminportenum, mprapi/MprAdminPortEnum, rras.mpradminportenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
-	MprAdminPortEnum
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminPortEnum function


## -description


The 
<b>MprAdminPortEnum</b> function enumerates all active ports in a specific connection, or all ports available for use or currently used by RAS.


## -parameters




### -param hRasServer [in]

A handle to the RAS server whose ports are to be enumerated. To obtain this handle, call <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.


### -param hRasConnection

TBD


### -param lplpbBuffer [out]

On successful completion, a pointer to an array of <a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a> structures that describes the port. Free this memory by calling 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>. 


### -param dwPrefMaxLen [in]

A value that specifies the preferred maximum length of returned data, in 8-bit bytes. If this parameter is -1, the buffer that is returned is large enough to hold all available data.


### -param lpdwEntriesRead [out]

A pointer to a <b>DWORD</b> variable. This variable receives the total number of ports that are enumerated from the current resume position.


### -param lpdwTotalEntries [out]

A pointer to a <b>DWORD</b> variable. This variable receives the total number of ports that could have been enumerated from the current resume position.


### -param lpdwResumeHandle [in]

A pointer to a <b>DWORD</b> variable. On successful execution, this parameter specifies a handle that can be used to resume the enumeration. This parameter should be zero on the first call and left unchanged on subsequent calls. If the return code is <b>ERROR_MORE_DATA</b>, the call can be reissued with the handle to retrieve more data. If the handle is <b>NULL</b> on return, the enumeration cannot be continued. This handle is invalid for other types of error returns.


#### - hConnection [in]

A handle to a connection for which the active ports are enumerated. If this parameter is <b>INVALID_HANDLE_VALUE</b>, all the ports in use or available for use by RRAS are enumerated. To obtain this handle, call 
<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the error codes listed in the following table.

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
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running, possibly because the Dynamic Interface Manager (DIM) is configured to run only on a LAN.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following parameters is <b>NULL</b> or does not point to valid memory: <i>lplpBuffer</i>, <i>lpdwEntriesRead</i>, or <i>lpdwTotalEntries</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Not all of the data was returned with this call. To obtain additional data, call the function again using the handle that was returned in the <i>IpdwResumeHandle</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> parameter is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hConnection</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>
 




## -remarks



If the RRAS redistributable is installed, this function is available on Windows NT 4.0. However, the version of Mprapi.dll that is provided with the RRAS redistributable exports the function as 
<b>RasAdminPortEnum</b> rather than 
<b>MprAdminPortEnum</b>. Therefore, when using the RRAS redistributable, use 
<a href="_win32_loadlibrary">LoadLibrary</a> and 
<a href="_win32_getprocaddress">GetProcAddress</a> to access this function.




## -see-also




<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

