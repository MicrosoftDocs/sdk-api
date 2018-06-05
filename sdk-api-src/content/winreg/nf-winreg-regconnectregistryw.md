---
UID: NF:winreg.RegConnectRegistryW
title: RegConnectRegistryW function
author: windows-sdk-content
description: Establishes a connection to a predefined registry key on another computer.
old-location: base\regconnectregistry.htm
old-project: SysInfo
ms.assetid: d7fb41cc-4855-4ad7-879c-b1ac85ac5803
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: RegConnectRegistry, RegConnectRegistry function, RegConnectRegistryA, RegConnectRegistryW, _win32_regconnectregistry, base.regconnectregistry, winreg/RegConnectRegistry, winreg/RegConnectRegistryA, winreg/RegConnectRegistryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Registry-l2-1-0.dll
-	advapi32legacy.dll
-	API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
-	RegConnectRegistry
-	RegConnectRegistryA
-	RegConnectRegistryW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegConnectRegistryW function


## -description


Establishes a connection to a predefined registry key on another computer.


## -parameters




### -param lpMachineName [in, optional]

The name of the remote computer. The string has the following form: 




\\<i>computername</i>

The caller must have access to the remote computer or the function fails.

If this parameter is <b>NULL</b>, the local computer name is used.


### -param hKey [in]

A predefined registry handle. This parameter can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a> on the remote computer. 




<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_PERFORMANCE_DATA</b>
<b>HKEY_USERS</b>

### -param phkResult [out]

A pointer to a variable that receives a key handle identifying the predefined handle on the remote computer.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



<b>RegConnectRegistry</b> requires the Remote Registry service to be running on the remote computer. By default, this service is configured to be started manually. To configure the Remote Registry service to start automatically, run Services.msc and change the Startup Type of the service to Automatic.

<b>Windows Server 2003 and Windows XP/2000:  </b>The Remote Registry service is configured to start automatically by default.

When a handle returned by 
<b>RegConnectRegistry</b> is no longer needed, it should be closed by calling 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>.

If the computer is joined to a workgroup and the "Force network logons using local accounts to authenticate as Guest" policy is enabled, the function fails. Note that this policy is enabled by default if the  computer is joined to a workgroup.

If the current user does not have proper access to the remote computer, the call to <b>RegConnectRegistry</b> fails. To connect to a remote registry, call <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> with LOGON32_LOGON_NEW_CREDENTIALS and <a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> before calling <b>RegConnectRegistry</b>.

<b>Windows 2000:  </b>One possible workaround is to establish a session to an administrative share such as IPC$ using a different set of credentials. To specify credentials other than those of the current user, use the <a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a> function to connect to the share. When you have finished accessing the registry, cancel the connection. 

<b>Windows XP Home Edition:  </b>You cannot use this function  to connect to a remote computer running Windows XP Home Edition. This function does work with the name of the local computer even if it is running Windows XP Home Edition because this bypasses the authentication layer.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

