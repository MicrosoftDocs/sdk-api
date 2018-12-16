---
UID: NF:winreg.RegOpenKeyW
title: RegOpenKeyW function
author: windows-sdk-content
description: Opens the specified registry key.
old-location: base\regopenkey.htm
tech.root: sysinfo
ms.assetid: bad0a0f8-1889-4eff-98be-084c95d69f3b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegOpenKey, RegOpenKey function, RegOpenKeyA, RegOpenKeyW, _win32_regopenkey, base.regopenkey, winreg/RegOpenKey, winreg/RegOpenKeyA, winreg/RegOpenKeyW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegOpenKeyW (Unicode) and RegOpenKeyA (ANSI)
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
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegOpenKey
 - RegOpenKeyA
 - RegOpenKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegOpenKeyW function


## -description


Opens the specified registry key.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function.</div><div> </div>

## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:

<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry key to be opened. This key must be a subkey of the key identified by the <i>hKey</i> parameter. 

Key names are not case sensitive.

If this parameter is <b>NULL</b> or a pointer to an empty string, the function returns the same handle that was passed in.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function after you have finished using the handle.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The 
<b>RegOpenKey</b> function uses the default security access mask to open a key. If opening the key requires a different access right, the function fails, returning ERROR_ACCESS_DENIED. An application should use the 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function to specify an access mask in this situation.

<b>RegOpenKey</b> does not create the specified key if the key does not exist in the database.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://msdn.microsoft.com/10a8cbfb-52dc-436a-827e-78f12eb62af0">RegOpenCurrentUser</a> function.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

