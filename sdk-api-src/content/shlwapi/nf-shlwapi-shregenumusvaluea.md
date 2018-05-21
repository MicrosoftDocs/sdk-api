---
UID: NF:shlwapi.SHRegEnumUSValueA
title: SHRegEnumUSValueA function
author: windows-driver-content
description: Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegEnumUSValue.htm
old-project: shell
ms.assetid: 78ba5df4-8ee3-473f-b3ef-0bca65bb0a2a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: SHRegEnumUSValue, SHRegEnumUSValue function [Windows Shell], SHRegEnumUSValueA, SHRegEnumUSValueW, _win32_SHRegEnumUSValue, shell.SHRegEnumUSValue, shlwapi/SHRegEnumUSValue, shlwapi/SHRegEnumUSValueA, shlwapi/SHRegEnumUSValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegEnumUSValueW (Unicode) and SHRegEnumUSValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-Registryuserspecific-l1-1-0.dll
-	KernelBase.dll
api_name:
-	SHRegEnumUSValue
-	SHRegEnumUSValueA
-	SHRegEnumUSValueW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHRegEnumUSValueA function


## -description


Enumerates the values of the specified registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSkey

TBD


### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the value to retrieve. This parameter should be zero for the first call and incremented for subsequent calls.


### -param pszValueName [out]

Type: <b>LPTSTR</b>

A pointer to a character buffer that receives the enumerated value name. The size of this buffer is specified in <i>pcchValueNameLen</i>.


### -param pcchValueName

TBD


### -param pdwType [out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the data type of the value. These are the same values as those described under the <i>lpType</i> parameter of <a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a>.


### -param pvData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that receives the data for the value entry. The size of this buffer is specified in <i>pcbData</i>. This parameter can be <b>NULL</b> if the data is not required.


### -param pcbData [in, out, optional]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pvData</i>. On exit, this contains the number of bytes that were copied to <i>pvData</i>.


### -param enumRegFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/4216a983-9d53-44b1-8273-e5a90ac4b3ef">SHREGENUM_FLAGS</a> that specifies the base key in which the enumeration should take place.


#### - hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


#### - pcchValueNameLen [in, out]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that, on entry, contains the size of the buffer at <i>pszValueName</i>, in characters. On exit, this contains the number of characters that were copied to <i>pszValueName</i>.


## -returns



Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a textual description of the error.



