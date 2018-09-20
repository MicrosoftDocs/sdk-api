---
UID: NF:oleacc.GetStateTextW
title: GetStateTextW function
author: windows-sdk-content
description: Retrieves a localized string that describes an object's state for a single predefined state bit flag. Because state values are a combination of one or more bit flags, clients call this function more than once to retrieve all state strings.
old-location: winauto\getstatetext.htm
tech.root: WinAuto
ms.assetid: 2a136883-870e-48c3-b182-1cdc64768894
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetStateText, GetStateText function [Windows Accessibility], GetStateTextA, GetStateTextW, _msaa_GetStateText, msaa.getstatetext, oleacc/GetStateText, oleacc/GetStateTextA, oleacc/GetStateTextW, winauto.getstatetext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetStateTextW (Unicode) and GetStateTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - GetStateText
 - GetStateTextA
 - GetStateTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# GetStateTextW function


## -description


Retrieves a localized string that describes an object's state for a single predefined state bit flag. Because state values are a combination of one or more bit flags, clients call this function more than once to retrieve all state strings.


## -parameters




### -param lStateBit [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One of the <a href="https://msdn.microsoft.com/1253d2d2-d931-4380-9ae8-f4e1fdaee817">object state constants</a>.


### -param lpszState [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Address of a buffer that receives the state text string. If this parameter is <b>NULL</b>, the function returns the state string's length, not including the null character.


### -param cchState [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of the buffer that is pointed to by the <i>lpszStateBit</i> parameter. For ANSI strings, this value is measured in bytes; for Unicode strings, it is measured in characters.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

If successful, and if <i>lpszStateBit</i> is non-<b>NULL</b>, the return value is the number of bytes (ANSI strings) or characters (Unicode strings) that are copied into the buffer, not including the null-terminated character. If <i>lpszStateBit</i> is <b>NULL</b>, the return value represents the string's length, not including the null character.

If the string resource does not exist, or if the <i>lpszStateBit</i> parameter is not a valid pointer, the return value is zero (0). To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function accepts only one state bit at a time, not a bitmask.



