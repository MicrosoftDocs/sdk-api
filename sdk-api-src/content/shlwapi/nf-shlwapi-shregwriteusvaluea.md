---
UID: NF:shlwapi.SHRegWriteUSValueA
title: SHRegWriteUSValueA function
author: windows-sdk-content
description: Writes a value to a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegWriteUSValue.htm
old-project: shell
ms.assetid: f94569c6-415b-4263-bab4-8a5baca47901
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: REG_BINARY, REG_DWORD, REG_DWORD_BIG_ENDIAN, REG_DWORD_LITTLE_ENDIAN, REG_EXPAND_SZ, REG_FULL_RESOURCE_DESCRIPTOR, REG_LINK, REG_MULTI_SZ, REG_NONE, REG_QWORD, REG_QWORD_LITTLE_ENDIAN, REG_RESOURCE_LIST, REG_RESOURCE_REQUIREMENTS_LIST, REG_SZ, SHREGSET_DEFAULT, SHREGSET_FORCE_HKCU, SHREGSET_FORCE_HKLM, SHREGSET_HKCU, SHREGSET_HKLM, SHRegWriteUSValue, SHRegWriteUSValue function [Windows Shell], SHRegWriteUSValueA, SHRegWriteUSValueW, _win32_SHRegWriteUSValue, shell.SHRegWriteUSValue, shlwapi/SHRegWriteUSValue, shlwapi/SHRegWriteUSValueA, shlwapi/SHRegWriteUSValueW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegWriteUSValueW (Unicode) and SHRegWriteUSValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-Registryuserspecific-l1-1-0.dll
 - KernelBase.dll
api_name:
 - SHRegWriteUSValue
 - SHRegWriteUSValueA
 - SHRegWriteUSValueW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHRegWriteUSValueA function


## -description


Writes a value to a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


### -param pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the name of the value. This value is an entry in the subkey specified by <i>hUSKey</i>. If a value with this name is not already present in the subkey, it will be added.

                        

If this parameter is <b>NULL</b> or an empty string, the function sets the type and data for the subkey's Default value.


### -param dwType [in]

Type: <b>DWORD</b>

The type of the data to be stored in the value specified by <i>pszValue</i>. One of the following registry value types defined in Winnt.h and Wdm.h.



#### REG_NONE (0x00000000)



#### REG_SZ (0x00000001)



#### REG_EXPAND_SZ (0x00000002)



#### REG_BINARY (0x00000003)



#### REG_DWORD (0x00000004)



#### REG_DWORD_LITTLE_ENDIAN (0x00000004)



#### REG_DWORD_BIG_ENDIAN (0x00000005)



#### REG_LINK (0x00000006)



#### REG_MULTI_SZ (0x00000007)



#### REG_RESOURCE_LIST (0x00000008)



#### REG_FULL_RESOURCE_DESCRIPTOR (0x00000009)



#### REG_RESOURCE_REQUIREMENTS_LIST (0x0000000A)



#### REG_QWORD (0x0000000B)



#### REG_QWORD_LITTLE_ENDIAN (0x0000000B)


### -param pvData [in]

Type: <b>const void*</b>

A pointer to the data to be set for the value specified by <i>pszValue</i>. For string-based types, such as REG_SZ, the string must be null-terminated. With the REG_MULTI_SZ data type, the string must be terminated with two null characters. A backslash in a path must be preceded by another backslash as an escape character. For example, specify "C:\\mydir\\myfile" to store the string "C:\mydir\myfile".


### -param cbData [in]

Type: <b>DWORD</b>

The size, in bytes, of the data pointed to by the <i>pvData</i> parameter. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, <i>cbData</i> must include the size of the terminating null character or characters.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that indicate the subtree to which the data should be written. One or more of the following values:



#### SHREGSET_HKCU (0x00000001)

Write to <b>HKEY_CURRENT_USER</b> only if a value of the name specified in <i>pszValue</i> does not currently exist under the specified subkey.



#### SHREGSET_FORCE_HKCU (0x00000002)

Write to <b>HKEY_CURRENT_USER</b>. If a value of the name specified in <i>pszValue</i> already exists, it will be overwritten.



#### SHREGSET_HKLM (0x00000004)

Write to <b>HKEY_LOCAL_MACHINE</b> only if a value of the name specified in <i>pszValue</i> does not currently exist under the specified subkey..



#### SHREGSET_FORCE_HKLM (0x00000008)

Write to <b>HKEY_LOCAL_MACHINE</b>. If a value of the name specified in <i>pszValue</i> already exists, it will be overwritten.



#### SHREGSET_DEFAULT (0x00000006)

Equivalent to (<b>SHREGSET_FORCE_HKCU</b> | <b>SHREGSET_HKLM</b>).


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful; otherwise, a nonzero error code defined in Winerror.h. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -remarks



To use <b>SHRegWriteUSValue</b>, you must first open the key with <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a>. Once the key is opened, you can use <b>SHRegWriteUSValue</b> as many times as necessary.

If you only need to write a single value, you should use <a href="https://msdn.microsoft.com/96559f8c-8527-4924-928e-f27049069407">SHRegSetUSValue</a>, which both opens the key and writes the value.

If you need to write more than one value on the same key, multiple calls to <b>SHRegWriteUSValue</b> are usually more efficient than <a href="https://msdn.microsoft.com/96559f8c-8527-4924-928e-f27049069407">SHRegSetUSValue</a>, because the key is only opened once.




## -see-also




<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>
 

 

