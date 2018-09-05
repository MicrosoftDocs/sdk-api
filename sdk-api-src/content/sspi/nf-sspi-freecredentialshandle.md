---
UID: NF:sspi.FreeCredentialsHandle
title: FreeCredentialsHandle function
author: windows-sdk-content
description: Notifies the security system that the credentials are no longer needed.
old-location: security\freecredentialshandle.htm
old-project: SecAuthN
ms.assetid: e089618c-8233-475a-9725-39265c6427ab
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FreeCredentialsHandle, FreeCredentialsHandle function [Security], _ssp_freecredentialshandle, security.freecredentialshandle, sspi/FreeCredentialsHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - FreeCredentialsHandle
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# FreeCredentialsHandle function


## -description


The <b>FreeCredentialsHandle</b> function notifies the security system that the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> are no longer needed. An application calls this function to free the credential handle acquired in the call to the 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function after calling the <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function to free any context handles associated with the credential. When all references to this credential set have been removed, the credentials themselves can be removed.

Failure to free credentials handles will result in memory leaks.


## -parameters




### -param phCredential [in]

A pointer to the <a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CredHandle</a> handle obtained by using the 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a>



<a href="authentication_functions.htm">SSPI Functions</a>
 

 

