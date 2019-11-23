---
UID: NF:winreg.RegDeleteKeyValueW
title: RegDeleteKeyValueW function (winreg.h)

description: Removes the specified value from the specified registry key and subkey.
old-location: base\regdeletekeyvalue.htm
tech.root: SysInfo
ms.assetid: a4a082c2-8cf3-41eb-87c0-a6c453821f8b

ms.date: 12/05/2018
ms.keywords: RegDeleteKeyValue, RegDeleteKeyValue function, RegDeleteKeyValueA, RegDeleteKeyValueW, base.regdeletekeyvalue, winreg/RegDeleteKeyValue, winreg/RegDeleteKeyValueA, winreg/RegDeleteKeyValueW
ms.topic: function
f1_keywords: 
 - "winreg/RegDeleteKeyValue"
dev_langs:
 - c++
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteKeyValueW (Unicode) and RegDeleteKeyValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - RegDeleteKeyValue
 - RegDeleteKeyValueA
 - RegDeleteKeyValueW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegDeleteKeyValueW function


## -description


Removes the specified  value from the specified registry key and subkey.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:


<pre xml:space="preserve"><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_USERS</b></pre>



### -param lpSubKey [in, optional]

The name of the registry key. This key must be a subkey of the key identified by the <i>hKey</i> parameter.


### -param lpValueName [in, optional]

The registry value to be removed from the key.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regsetkeyvaluea">RegSetKeyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
 

 

