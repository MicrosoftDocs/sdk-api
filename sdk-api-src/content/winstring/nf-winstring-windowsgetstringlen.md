---
UID: NF:winstring.WindowsGetStringLen
title: WindowsGetStringLen function
author: windows-sdk-content
description: Gets the length, in Unicode characters, of the specified string.
old-location: winrt\windowsgetstringlen.htm
old-project: WinRT
ms.assetid: 80B659DF-C760-4D9E-B779-144A5B8FEA59
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WindowsGetStringLen, WindowsGetStringLen function [Windows Runtime], winrt.windowsgetstringlen, winstring/WindowsGetStringLen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winstring.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winstring.h
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsGetStringLen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsGetStringLen function


## -description


Gets the length, in Unicode characters, of the specified string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string whose length is to be found.


## -returns



Type: <b>UINT32</b>

The number of Unicode characters in <i>string</i>, including embedded null characters, but excluding the terminating null; or 0 if <i>string</i> is <b>NULL</b>.



