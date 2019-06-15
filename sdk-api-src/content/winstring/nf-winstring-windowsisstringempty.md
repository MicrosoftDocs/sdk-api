---
UID: NF:winstring.WindowsIsStringEmpty
title: WindowsIsStringEmpty function (winstring.h)
author: windows-sdk-content
description: Indicates whether the specified string is the empty string.
old-location: winrt\windowsisstringempty.htm
tech.root: WinRT
ms.assetid: F354F692-4D64-4A3F-8B27-1951C93A6FCA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WindowsIsStringEmpty, WindowsIsStringEmpty function [Windows Runtime], winrt.windowsisstringempty, winstring/WindowsIsStringEmpty
ms.topic: function
f1_keywords: ["winstring/WindowsIsStringEmpty"]
req.header: winstring.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
 - WindowsIsStringEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WindowsIsStringEmpty function


## -description


Indicates whether the specified string is the empty string.


## -parameters




### -param string [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a></b>

The string to be tested for content.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if <i>string</i> is <b>NULL</b> or  the empty string; otherwise, <b>FALSE</b>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowsgetstringlen">WindowsGetStringLen</a>
 

 

