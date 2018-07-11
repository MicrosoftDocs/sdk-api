---
UID: NF:oleacc.GetRoleTextA
title: GetRoleTextA function
author: windows-sdk-content
description: Retrieves the localized string that describes the object's role for the specified role value.
old-location: winauto\getroletext.htm
old-project: WinAuto
ms.assetid: 58436001-92d7-4afa-af07-169c8bbda9ba
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetRoleText, GetRoleText function [Windows Accessibility], GetRoleTextA, GetRoleTextW, _msaa_GetRoleText, msaa.getroletext, oleacc/GetRoleText, oleacc/GetRoleTextA, oleacc/GetRoleTextW, winauto.getroletext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetRoleTextW (Unicode) and GetRoleTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - GetRoleText
 - GetRoleTextA
 - GetRoleTextW
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
---

# GetRoleTextA function


## -description


Retrieves the localized string that describes the object's role for the specified role value.


## -parameters




### -param lRole

TBD


### -param lpszRole [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Address of a buffer that receives the role text string. If this parameter is <b>NULL</b>, the function returns the role string's length, not including the null character.


### -param cchRoleMax [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of the buffer that is pointed to by the <i>lpszRole</i> parameter. For ANSI strings, this value is measured in bytes; for Unicode strings, it is measured in characters.


#### - dwRole [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One of the <a href="https://msdn.microsoft.com/f015252a-c0df-4a21-a995-ff2f6cafbab8">object role</a> constants.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

If successful, and if <i>lpszRole</i> is non-<b>NULL</b>, the return value is the number of bytes (ANSI strings) or characters (Unicode strings) copied into the buffer, not including the terminating null character. If <i>lpszRole</i> is <b>NULL</b>, the return value represents the string's length, not including the null character.

If the string resource does not exist, or if the <i>lpszRole</i> parameter is not a valid pointer, the return value is zero (0). To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



