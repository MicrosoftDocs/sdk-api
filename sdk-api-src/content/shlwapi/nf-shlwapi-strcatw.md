---
UID: NF:shlwapi.StrCatW
title: StrCatW function
author: windows-sdk-content
description: Appends one string to another.
old-location: shell\StrCat.htm
tech.root: shell
ms.assetid: fd357462-83be-42a8-9f39-1e023bd5f86e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: StrCat, StrCat function [Windows Shell], StrCatW, _win32_StrCat, shell.StrCat, shlwapi/StrCat, shlwapi/StrCatW
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
req.unicode-ansi: StrCatW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrCat
 - StrCatW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrCatW function


## -description


Appends one string to another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters




### -param psz1 [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string. When this function returns successfully, this string contains its original content with the string <i>psz2</i> appended. This buffer must be large enough to hold both strings and the terminating null character.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string to be appended to <i>psz1</i>.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>, which holds the combined strings.




## -remarks



<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Consider using one of the following alternatives: <a href="https://msdn.microsoft.com/6330483b-dc61-4bbf-8ee7-e91a93495bb2">StringCbCat</a>, <a href="https://msdn.microsoft.com/db9f0731-0f7b-4018-ad07-1abe0bfe71e8">StringCbCatEx</a>, <a href="https://msdn.microsoft.com/56ef4ada-52df-48dd-a5e1-f62311be7592">StringCbCatN</a>, <a href="https://msdn.microsoft.com/ad1cad70-c548-4b2f-b253-b0af5000df08">StringCbCatNEx</a>, <a href="https://msdn.microsoft.com/72ddb6ab-8167-4213-815b-bd15b62d6123">StringCchCat</a>, <a href="https://msdn.microsoft.com/3b829dfa-6ede-47bd-b4d7-fcbf94a26c50">StringCchCatEx</a>, <a href="https://msdn.microsoft.com/516b67f9-ab6e-4c23-b04a-01848de09115">StringCchCatN</a>, or <a href="https://msdn.microsoft.com/63c9f437-b769-4c5a-9168-d0c458947abc">StringCchCatNEx</a>. You should review <a href="https://msdn.microsoft.com/eca31652-2659-456d-b082-c84d6fd39094">Security Considerations: Microsoft Windows Shell</a> before continuing.



