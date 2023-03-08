---
UID: NC:ntsecapi.PSAM_INIT_NOTIFICATION_ROUTINE
title: PSAM_INIT_NOTIFICATION_ROUTINE (ntsecapi.h)
description: The InitializeChangeNotify function is implemented by a password filter DLL. This function initializes the DLL.
helpviewer_keywords: ["InitializeChangeNotify","InitializeChangeNotify callback function [Security]","PSAM_INIT_NOTIFICATION_ROUTINE","PSAM_INIT_NOTIFICATION_ROUTINE callback","_pswd_initializechangenotify","ntsecapi/InitializeChangeNotify","security.initializechangenotify"]
old-location: security\initializechangenotify.htm
tech.root: security
ms.assetid: c503c849-65da-4514-b6d9-a95c9d75433e
ms.date: 12/05/2018
ms.keywords: InitializeChangeNotify, InitializeChangeNotify callback function [Security], PSAM_INIT_NOTIFICATION_ROUTINE, PSAM_INIT_NOTIFICATION_ROUTINE callback, _pswd_initializechangenotify, ntsecapi/InitializeChangeNotify, security.initializechangenotify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSAM_INIT_NOTIFICATION_ROUTINE
 - ntsecapi/PSAM_INIT_NOTIFICATION_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecapi.h
api_name:
 - InitializeChangeNotify
---

# PSAM_INIT_NOTIFICATION_ROUTINE callback function


## -description

The <b>InitializeChangeNotify</b> function is implemented by a password filter DLL. This function initializes the DLL.

## -parameters

### -param unnamedParam1

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

<b>InitializeChangeNotify</b> is called by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) to verify that the password notification DLL is loaded and initialized.

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
<a href="/windows/desktop/SecMgmt/password-filter-programming-considerations">Password Filter Programming Considerations</a>
</td>
</tr>
<tr>
<td>How to install and register your own password filter DLL</td>
<td>
<a href="/windows/desktop/SecMgmt/installing-and-registering-a-password-filter-dll">Installing and Registering a Password Filter DLL</a>
</td>
</tr>
<tr>
<td>The password filter DLL provided by Microsoft</td>
<td>
<a href="/windows/desktop/SecMgmt/strong-password-enforcement-and-passfilt-dll">Strong Password Enforcement and Passfilt.dll</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_password_notification_routine">PasswordChangeNotify</a>



<a href="/windows/desktop/api/ntsecapi/nc-ntsecapi-psam_password_filter_routine">PasswordFilter</a>