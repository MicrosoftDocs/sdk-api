---
UID: NF:mprapi.MprAdminServerGetCredentials
title: MprAdminServerGetCredentials function
author: windows-driver-content
description: The MprAdminServerGetCredentials function retrieves the pre-shared key for the specified server.
old-location: rras\mpradminservergetcredentials.htm
old-project: RRAS
ms.assetid: 76211b14-8f6c-48e4-846f-bd5d3a04285d
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MprAdminServerGetCredentials, MprAdminServerGetCredentials function [RAS], _mpr_mpradminservergetcredentials, mprapi/MprAdminServerGetCredentials, rras.mpradminservergetcredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	MprAdminServerGetCredentials
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminServerGetCredentials function


## -description


The 
<b>MprAdminServerGetCredentials</b> function retrieves the pre-shared key for the specified server.


## -parameters




### -param hMprServer [in]

Handle to a Windows server. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.


### -param lplpbBuffer [out]

On successful completion, a pointer to an <a href="https://msdn.microsoft.com/b37b9589-5c25-44ac-954a-c9fb2c2ee503">MPR_CREDENTIALSEX_1</a> structure that contains the pre-shared key for the server. Free the memory occupied by this structure with 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpbBuffer</i> parameter is <b>NULL</b>.

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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



The server maintains a single pre-shared key for all users.




## -see-also




<a href="https://msdn.microsoft.com/b37b9589-5c25-44ac-954a-c9fb2c2ee503">MPR_CREDENTIALSEX_1</a>



<a href="https://msdn.microsoft.com/cc77007f-306f-467a-a52f-bf920da15e74">MprAdminServerSetCredentials</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

