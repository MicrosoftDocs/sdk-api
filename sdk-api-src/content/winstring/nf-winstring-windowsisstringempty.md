---
UID: NF:winstring.WindowsIsStringEmpty
title: WindowsIsStringEmpty function
author: windows-driver-content
description: Indicates whether the specified string is the empty string.
old-location: winrt\windowsisstringempty.htm
old-project: WinRT
ms.assetid: F354F692-4D64-4A3F-8B27-1951C93A6FCA
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: WindowsIsStringEmpty, WindowsIsStringEmpty function [Windows Runtime], winrt.windowsisstringempty, winstring/WindowsIsStringEmpty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	winstring.h
-	API-MS-Win-Core-WinRT-String-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
-	WindowsIsStringEmpty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsIsStringEmpty function


## -description


Indicates whether the specified string is the empty string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string to be tested for content.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if <i>string</i> is <b>NULL</b> or  the empty string; otherwise, <b>FALSE</b>. 




## -see-also




<a href="https://msdn.microsoft.com/80B659DF-C760-4D9E-B779-144A5B8FEA59">WindowsGetStringLen</a>
 

 

