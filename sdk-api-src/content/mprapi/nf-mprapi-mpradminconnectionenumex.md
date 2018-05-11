---
UID: NF:mprapi.MprAdminConnectionEnumEx
title: MprAdminConnectionEnumEx function
author: windows-driver-content
description: The MprAdminConnectionEnumEx function enumerates the active connections for a specified RRAS server.
old-location: rras\mpradminconnectionenumex.htm
old-project: RRAS
ms.assetid: 12507432-bf18-444d-9bcc-4ebc1418c083
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprAdminConnectionEnumEx, MprAdminConnectionEnumEx function [RAS], mprapi/MprAdminConnectionEnumEx, rras.mpradminconnectionenumex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
-	MprAdminConnectionEnumEx
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminConnectionEnumEx function


## -description


The 
<b>MprAdminConnectionEnumEx</b> function enumerates the active connections for a specified RRAS server.


## -parameters




### -param hRasServer [in]

A handle to the RAS server on which connections are enumerated. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param pObjectHeader [in]

A pointer to an <a href="https://msdn.microsoft.com/2f4e1ddc-7991-4091-9889-fdd2d75e702f">MPRAPI_OBJECT_HEADER</a>   structure that specifies the structure version received by <i>ppRasConn</i>.


### -param dwPreferedMaxLen [in]

A value that specifies the preferred maximum length of returned data in 8-bit bytes. If <i>dwPrefMaxLen</i> is -1, the buffer returned is large enough to hold all available information.


### -param lpdwEntriesRead [out]

A pointer to a <b>DWORD</b> that receives the total number of connections enumerated from the current resume position.


### -param lpdwTotalEntries [out]

A pointer to a <b>DWORD</b> that receives the total number of connections that could have been enumerated from the current resume position.


### -param ppRasConn [out]

A pointer, on output, to an array of <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structures that contain the active connection information for the RRAS server in  <i>hRasServer</i>. The number of array elements is determined by the value pointed to by <i>lpdwEntriesRead</i>.


### -param lpdwResumeHandle [in]

A pointer to a <b>DWORD</b> variable that specifies a resume handle used to continue the enumeration. The <i>lpdwResumeHandle</i> parameter is <b>NULL</b> on the first call, and left unchanged on subsequent calls. If the return code is <b>ERROR_MORE_DATA</b>, another call may be made using this handle to retrieve more data. If the handle is <b>NULL</b> upon return, the enumeration is complete. This handle is invalid for other types of error returns.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

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
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Not all of the data was returned with this call. To obtain additional data, call the function again using the resume handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PROC_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified procedure could not be found.

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



The caller should free the memory pointed to by <i>ppRasConn</i> by calling the function <a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

