---
UID: NF:shlwapi.SHRegDeleteEmptyUSKeyW
title: SHRegDeleteEmptyUSKeyW function
author: windows-driver-content
description: Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegDeleteEmptyUSKey.htm
old-project: shell
ms.assetid: adb09a2b-674c-472d-9f16-8e150476f1f5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SHRegDeleteEmptyUSKey, SHRegDeleteEmptyUSKey function [Windows Shell], SHRegDeleteEmptyUSKeyA, SHRegDeleteEmptyUSKeyW, _win32_SHRegDeleteEmptyUSKey, shell.SHRegDeleteEmptyUSKey, shlwapi/SHRegDeleteEmptyUSKey, shlwapi/SHRegDeleteEmptyUSKeyA, shlwapi/SHRegDeleteEmptyUSKeyW
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
req.unicode-ansi: SHRegDeleteEmptyUSKeyW (Unicode) and SHRegDeleteEmptyUSKeyA (ANSI)
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
-	SHRegDeleteEmptyUSKey
-	SHRegDeleteEmptyUSKeyA
-	SHRegDeleteEmptyUSKeyW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHRegDeleteEmptyUSKeyW function


## -description


Deletes an empty registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


### -param pwzSubKey

TBD


### -param delRegFlags [in]

Type: <b><a href="https://msdn.microsoft.com/90a8bf22-f62b-4027-8219-7a5ead6577da">SHREGDEL_FLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/90a8bf22-f62b-4027-8219-7a5ead6577da">SHREGDEL_FLAGS</a> that specifies from which base key the subkey will be deleted.


#### - pszValue [in]

Type: <b>LPCSTR</b>

A pointer to  the null-terminated string that specifies the empty user-defined registry subkey to be deleted.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -see-also




<a href="https://msdn.microsoft.com/f70407af-d8ee-4333-be32-01887d4add4c">SHRegDeleteUSValue</a>
 

 

