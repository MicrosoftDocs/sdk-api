---
UID: NF:winuser.RegisterClassExA
title: RegisterClassExA function
author: windows-sdk-content
description: Registers a window class for subsequent use in calls to the CreateWindow or CreateWindowEx function.
old-location: winmsg\registerclassex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\registerclassex.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: RegisterClassEx, RegisterClassEx function [Windows and Messages], RegisterClassExA, RegisterClassExW, _win32_RegisterClassEx, _win32_registerclassex_cpp, winmsg.registerclassex, winui._win32_registerclassex, winuser/RegisterClassEx, winuser/RegisterClassExA, winuser/RegisterClassExW
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
req.unicode-ansi: RegisterClassExW (Unicode) and RegisterClassExA (ANSI)
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - RegisterClassEx
 - RegisterClassExA
 - RegisterClassExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegisterClassExA function


## -description


Registers a window class for subsequent use in calls to the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function. 


## -parameters




### -param WNDCLASSEXA

TBD




#### - lpwcx [in]

Type: <b>const WNDCLASSEX*</b>

A pointer to a <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure. You must fill the structure with the appropriate class attributes before passing it to the function. 


## -returns



Type: <strong>Type: <b>ATOM</b>
</strong>

If the function succeeds, the return value is a class atom that uniquely identifies the class being registered. This atom can only be used by the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>, <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>, <a href="https://msdn.microsoft.com/f7eb12c9-ff24-465d-8c6d-8ee5777c05bc">GetClassInfo</a>, <a href="https://msdn.microsoft.com/a353eaa2-7a79-4008-84fe-a72847350745">GetClassInfoEx</a>, <a href="https://msdn.microsoft.com/8240f00c-5772-4f6e-b05f-3e5a5b0efa27">FindWindow</a>, <a href="https://msdn.microsoft.com/f8d81dd7-1acc-405b-8970-8e708acccbf7">FindWindowEx</a>, and <a href="https://msdn.microsoft.com/ce0277a9-082e-49ef-b8fd-779284303ffa">UnregisterClass</a> functions and the <b>IActiveIMMap::FilterClientWindows</b> method. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If you register the window class by using 
				<b>RegisterClassExA</b>, the application tells the system that the windows of the created class expect messages with text or character parameters to use the ANSI character set; if you register it by using 
				<b>RegisterClassExW</b>, the application requests that the system pass text parameters of messages as Unicode. The <a href="https://msdn.microsoft.com/c1a4da81-1bed-4c79-bb3f-7f5d2fa5c8f9">IsWindowUnicode</a> function enables applications to query the nature of each window. For more information on ANSI and Unicode functions, see <a href="https://msdn.microsoft.com/601d24b0-11bb-48fa-a257-207c3acee226">Conventions for Function Prototypes</a>.

All window classes that an application registers are unregistered when it terminates. 

No window classes registered by a DLL are unregistered when the DLL is unloaded. A DLL must explicitly unregister its classes when it is unloaded. 



#### Examples

For an example, see <a href="https://msdn.microsoft.com/ea9e36c9-b10d-441e-b1b5-1ab93e009e1d">Using Window Classes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/8240f00c-5772-4f6e-b05f-3e5a5b0efa27">FindWindow</a>



<a href="https://msdn.microsoft.com/f8d81dd7-1acc-405b-8970-8e708acccbf7">FindWindowEx</a>



<a href="https://msdn.microsoft.com/f7eb12c9-ff24-465d-8c6d-8ee5777c05bc">GetClassInfo</a>



<a href="https://msdn.microsoft.com/a353eaa2-7a79-4008-84fe-a72847350745">GetClassInfoEx</a>



<a href="https://msdn.microsoft.com/039dd7cd-07cf-4c8a-9287-365d54da2f43">GetClassName</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a>



<a href="https://msdn.microsoft.com/ce0277a9-082e-49ef-b8fd-779284303ffa">UnregisterClass</a>



<a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>



<a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a>
 

 

