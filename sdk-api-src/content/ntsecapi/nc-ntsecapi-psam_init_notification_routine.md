---
UID: NC:ntsecapi.PSAM_INIT_NOTIFICATION_ROUTINE
title: PSAM_INIT_NOTIFICATION_ROUTINE
author: windows-sdk-content
description: The InitializeChangeNotify function is implemented by a password filter DLL. This function initializes the DLL.
old-location: security\initializechangenotify.htm
tech.root: secmgmt
ms.assetid: c503c849-65da-4514-b6d9-a95c9d75433e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InitializeChangeNotify, InitializeChangeNotify callback function [Security], PSAM_INIT_NOTIFICATION_ROUTINE, PSAM_INIT_NOTIFICATION_ROUTINE callback, _pswd_initializechangenotify, ntsecapi/InitializeChangeNotify, security.initializechangenotify
ms.topic: callback
req.header: ntsecapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecapi.h
api_name:
 - InitializeChangeNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSAM_INIT_NOTIFICATION_ROUTINE callback function


## -description


The <b>InitializeChangeNotify</b> function is implemented by a password filter DLL. This function initializes the DLL.


## -parameters




### -param Arg1








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
The password filter DLL is initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The password filter DLL is not initialized.

</td>
</tr>
</table>
 




## -remarks



<b>InitializeChangeNotify</b> is called by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) to verify that the password notification DLL is loaded and initialized.

This function must use the __stdcall calling convention, and must be exported by the DLL.

This function is called only for password filters that are installed and registered on a system.

Any process exception that is not handled within this function may cause security-related failures system-wide. Structured exception handling should be used when appropriate.

<table>
<tr>
<th>For information about</th>
<th>See</th>
</tr>
<tr>
<td>Programming issues when implementing a password filter DLL</td>
<td>
<a href="https://msdn.microsoft.com/ec7c1e7e-844a-43d4-b756-02bc1062d7b8">Password Filter Programming Considerations</a>
</td>
</tr>
<tr>
<td>How to install and register your own password filter DLL</td>
<td>
<a href="https://msdn.microsoft.com/12a6fe6d-5b37-4fcf-bd04-0a22d84ba323">Installing and Registering a Password Filter DLL</a>
</td>
</tr>
<tr>
<td>The password filter DLL provided by Microsoft</td>
<td>
<a href="https://msdn.microsoft.com/a84f83b2-181b-4f65-82bd-bc7f0689aad3">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81d34dff-3842-407b-8fd8-3b0a5a5f38f1">PasswordChangeNotify</a>



<a href="https://msdn.microsoft.com/cb4fe40e-81ea-4040-b3ee-642a093e5fca">PasswordFilter</a>
 

 

