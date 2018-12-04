---
UID: NF:winreg.RegLoadMUIStringA
title: RegLoadMUIStringA function
author: windows-sdk-content
description: Loads the specified string from the specified key and subkey.
old-location: base\regloadmuistring.htm
tech.root: sysinfo
ms.assetid: 76ffc77f-a1bc-4e01-858f-4a76563a2bbc
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: REG_MUI_STRING_TRUNCATE, RegLoadMUIString, RegLoadMUIString function, RegLoadMUIStringA, RegLoadMUIStringW, base.regloadmuistring, winreg/RegLoadMUIString, winreg/RegLoadMUIStringA, winreg/RegLoadMUIStringW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegLoadMUIStringW (Unicode) and RegLoadMUIStringA (ANSI)
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
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegLoadMUIString
 - RegLoadMUIStringA
 - RegLoadMUIStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegLoadMUIStringA function


## -description


Loads the specified string from the specified key and subkey.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param pszValue [in, optional]

The name of the registry value.


### -param pszOutBuf [out, optional]

A pointer to a buffer that receives the string.

Strings of the following form receive special handling:

@[<i>path</i>]\<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. If the <i>pszDirectory</i> parameter is not <b>NULL</b>, the directory is prepended to the path specified in the registry data. Note that <i>dllname</i> can contain environment variables to be expanded. 


### -param cbOutBuf [in]

The size of the <i>pszOutBuf</i> buffer, in bytes.


### -param pcbData [out, optional]

A pointer to a variable that receives the size of the data copied to the <i>pszOutBuf</i> buffer, in bytes.

If the buffer is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>pcbData</i>. In this case, the contents of the buffer are undefined.


### -param Flags [in]

This parameter can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_MUI_STRING_TRUNCATE"></a><a id="reg_mui_string_truncate"></a><dl>
<dt><b>REG_MUI_STRING_TRUNCATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The string is truncated to fit the available size of the <i>pszOutBuf</i> buffer. If this flag is specified, <i>pcbData</i> must be <b>NULL</b>.

</td>
</tr>
</table>
 


### -param pszDirectory [in, optional]

The directory path.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.

If the <i>pcbData</i> buffer is too small to receive the string, the function returns ERROR_MORE_DATA.

The ANSI version of this function returns ERROR_CALL_NOT_IMPLEMENTED.




## -remarks



The <b>RegLoadMUIString</b> function is supported only for Unicode. Although both Unicode (W) and ANSI (A) versions of this function are declared, the <b>RegLoadMUIStringA</b> function returns ERROR_CALL_NOT_IMPLEMENTED. Applications should explicitly call <b>RegLoadMUIStringW</b> or specify Unicode as the character set in platform invoke (PInvoke) calls. 

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

