---
UID: NF:winreg.RegConnectRegistryW
title: RegConnectRegistryW function (winreg.h)
description: Establishes a connection to a predefined registry key on another computer. (Unicode)
helpviewer_keywords: ["RegConnectRegistry", "RegConnectRegistry function", "RegConnectRegistryW", "_win32_regconnectregistry", "base.regconnectregistry", "winreg/RegConnectRegistry", "winreg/RegConnectRegistryW"]
old-location: base\regconnectregistry.htm
tech.root: winprog
ms.assetid: d7fb41cc-4855-4ad7-879c-b1ac85ac5803
ms.date: 12/05/2018
ms.keywords: RegConnectRegistry, RegConnectRegistry function, RegConnectRegistryA, RegConnectRegistryW, _win32_regconnectregistry, base.regconnectregistry, winreg/RegConnectRegistry, winreg/RegConnectRegistryA, winreg/RegConnectRegistryW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegConnectRegistryW (Unicode) and RegConnectRegistryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegConnectRegistryW
 - winreg/RegConnectRegistryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l2-3-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegConnectRegistry
 - RegConnectRegistryA
 - RegConnectRegistryW
---

# RegConnectRegistryW function


## -description

Establishes a connection to a predefined registry key on another computer.

## -parameters

### -param lpMachineName [in, optional]

The name of the remote computer. The string has the following form: 




&#92;&#92;<i>computername</i>

The caller must have access to the remote computer or the function fails.

If this parameter is <b>NULL</b>, the local computer name is used.

### -param hKey [in]

A predefined registry handle. This parameter can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a> on the remote computer. 




<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_PERFORMANCE_DATA</b>
<b>HKEY_USERS</b>

### -param phkResult [out]

A pointer to a variable that receives a key handle identifying the predefined handle on the remote computer.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

<b>RegConnectRegistry</b> requires the Remote Registry service to be running on the remote computer. By default, this service is configured to be started manually. To configure the Remote Registry service to start automatically, run Services.msc and change the Startup Type of the service to Automatic.

<b>Windows Server 2003 and Windows XP/2000:  </b>The Remote Registry service is configured to start automatically by default.

When a handle returned by 
<b>RegConnectRegistry</b> is no longer needed, it should be closed by calling 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

If the computer is joined to a workgroup and the "Force network logons using local accounts to authenticate as Guest" policy is enabled, the function fails. Note that this policy is enabled by default if the  computer is joined to a workgroup.

If the current user does not have proper access to the remote computer, the call to <b>RegConnectRegistry</b> fails. To connect to a remote registry, call <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> with LOGON32_LOGON_NEW_CREDENTIALS and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a> before calling <b>RegConnectRegistry</b>.

<b>Windows 2000:  </b>One possible workaround is to establish a session to an administrative share such as IPC$ using a different set of credentials. To specify credentials other than those of the current user, use the <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a> function to connect to the share. When you have finished accessing the registry, cancel the connection. 

<b>Windows XP Home Edition:  </b>You cannot use this function  to connect to a remote computer running Windows XP Home Edition. This function does work with the name of the local computer even if it is running Windows XP Home Edition because this bypasses the authentication layer.





> [!NOTE]
> The winreg.h header defines RegConnectRegistry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
