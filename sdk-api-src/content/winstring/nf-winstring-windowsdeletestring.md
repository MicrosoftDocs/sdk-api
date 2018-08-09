---
UID: NF:winstring.WindowsDeleteString
title: WindowsDeleteString function
author: windows-sdk-content
description: Decrements the reference count of a string buffer.
old-location: winrt\windowsdeletestring.htm
old-project: WinRT
ms.assetid: 79B9E5CF-396C-45FB-931B-7B50281A0446
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WindowsDeleteString, WindowsDeleteString function [Windows Runtime], winrt.windowsdeletestring, winstring/WindowsDeleteString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WindowsDeleteString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsDeleteString function


## -description


Decrements the reference count of a string buffer.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string to be deleted. If <i>string</i> is a fast-pass string created by <a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a>, or if <i>string</i> is <b>NULL</b> or empty, no action is taken and <b>S_OK</b> is returned.


## -returns



Type: <b>HRESULT</b>

This function always returns <b>S_OK</b>.




## -remarks



Use the <b>WindowsDeleteString</b> function to de-allocate an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>. Calling <b>WindowsDeleteString</b> decrements the reference count of the backing buffer, and if the reference count reaches 0, the Windows Runtime de-allocates the buffer.




## -see-also




<a href="https://msdn.microsoft.com/CACEFB80-A47E-45A7-9E13-29C1326B9453">WindowsCreateString</a>



<a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a>
 

 

