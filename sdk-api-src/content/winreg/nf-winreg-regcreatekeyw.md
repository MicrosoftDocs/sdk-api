---
UID: NF:winreg.RegCreateKeyW
title: RegCreateKeyW function
author: windows-driver-content
description: Creates the specified registry key. If the key already exists in the registry, the function opens it.
old-location: base\regcreatekey.htm
old-project: SysInfo
ms.assetid: cb4d30f4-e288-41e8-86e0-807c313db53d
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: RegCreateKey, RegCreateKey function, RegCreateKeyA, RegCreateKeyW, _win32_regcreatekey, base.regcreatekey, winreg/RegCreateKey, winreg/RegCreateKeyA, winreg/RegCreateKeyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegCreateKeyW (Unicode) and RegCreateKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
-	RegCreateKey
-	RegCreateKeyA
-	RegCreateKeyW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegCreateKeyW function


## -description


Creates the specified registry key. If the key already exists in the registry, the function opens it.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> function. However, applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.</div><div> </div>

## -parameters




### -param hKey [in]

A handle to an open registry key. The calling process  must have KEY_CREATE_SUB_KEY access to the key. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




Access for key creation is checked against the security descriptor of the registry key, not the access mask specified when the handle was obtained. Therefore, even if <i>hKey</i> was opened with a <i>samDesired</i> of KEY_READ, it   can be used in operations that create keys if allowed by its security descriptor.

This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param lpSubKey [in, optional]

The name of a key that this function opens or creates. This key must be a subkey of the key identified by the <i>hKey</i> parameter. 


For more information on key names, see <a href="https://msdn.microsoft.com/4ed60563-73d8-4134-8cb2-8388734fb18d">Structure of the Registry</a>.

If <i>hKey</i> is one of the predefined keys, <i>lpSubKey</i> may be <b>NULL</b>. In that case, <i>phkResult</i> receives the same <i>hKey</i> handle passed in to the function.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened or created key. If the key is not one of the predefined registry keys, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function after you have finished using the handle.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



An application cannot create a key that is a direct child of <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b>. An application can create subkeys in lower levels of the <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> trees.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://msdn.microsoft.com/10a8cbfb-52dc-436a-827e-78f12eb62af0">RegOpenCurrentUser</a> function.

The <b>RegCreateKey</b> function creates all missing keys in the specified path. An application can take advantage of this behavior to create several keys at once. For example, an application can create a subkey four levels deep at the same time as the three preceding subkeys by specifying a string of the following form for the <i>lpSubKey</i> parameter:

<i>subkey1\subkey2\subkey3\subkey4
			</i>

Note that this behavior will result in creation of unwanted keys if an existing key in the path is spelled incorrectly. 




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

