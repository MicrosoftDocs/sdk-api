---
UID: NF:winuser.CloseDesktop
title: CloseDesktop function
author: windows-sdk-content
description: Closes an open handle to a desktop object.
old-location: winstation\closedesktop.htm
old-project: winstation
ms.assetid: 861e57b2-061c-4598-ad38-6aef7b79ca54
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: CloseDesktop, CloseDesktop function [Windows Stations and Desktops], _win32_closedesktop, base.closedesktop, winstation.closedesktop, winuser/CloseDesktop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - api-ms-win-rtcore-ntuser-windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - CloseDesktop
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CloseDesktop function


## -description


Closes an open handle to a desktop object.


## -parameters




### -param hDesktop [in]

A handle to the desktop to be closed. This can be a handle returned by the 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>, 
<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>, or 
<a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a> functions. Do not specify the handle returned by the <a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>CloseDesktop</b> function will fail if any thread in the calling process is using the specified desktop handle or if the handle refers to the initial desktop of the calling process.




## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

