---
UID: NS:winuser.tagRAWINPUT
title: tagRAWINPUT
author: windows-sdk-content
description: Contains the raw input from a device.
old-location: inputdev\rawinput.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinput.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*LPRAWINPUT, *PRAWINPUT, LPRAWINPUT, LPRAWINPUT structure pointer [Keyboard and Mouse Input], PRAWINPUT, PRAWINPUT structure pointer [Keyboard and Mouse Input], RAWINPUT, RAWINPUT structure [Keyboard and Mouse Input], _win32_RAWINPUT_str, _win32_rawinput_str_cpp, inputdev.rawinput, tagRAWINPUT, winui._win32_rawinput_str, winuser/LPRAWINPUT, winuser/PRAWINPUT, winuser/RAWINPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: RAWINPUT, *PRAWINPUT, *LPRAWINPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWINPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagRAWINPUT structure


## -description


Contains the raw input from a device. 


## -struct-fields




### -field header

Type: <b><a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a></b>

The raw input data. 


### -field data


### -field data.mouse

<b>Type: <b><a href="https://msdn.microsoft.com/61925071-06b1-4471-8f34-7f1bd0c17d6d">RAWMOUSE</a></b>
</b>
If the data comes from a mouse, this is the raw input data. 


### -field data.keyboard

<b>Type: <b><a href="https://msdn.microsoft.com/536caca4-9368-486c-9ae4-6778497daf5f">RAWKEYBOARD</a></b>
</b>
If the data comes from a keyboard, this is the raw input data. 


### -field data.hid

<b>Type: <b><a href="https://msdn.microsoft.com/021d4b1a-69a9-482f-a796-21d74a98fbff">RAWHID</a></b>
</b>
If the data comes from an HID, this is the raw input data. 


## -remarks



The handle to this structure is passed in the <i>lParam</i> parameter of <a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>.

To get detailed information -- such as the header and the content of the raw input -- call <a href="https://msdn.microsoft.com/a2a15b77-58ef-4632-80dd-2770687c0e0f">GetRawInputData</a>.

To read the <b>RAWINPUT</b> in the message loop as a buffered read, call <a href="https://msdn.microsoft.com/a76d9b93-4faa-43c4-b72e-2ca9fc306703">GetRawInputBuffer</a>. 

To get device specific information, call <a href="https://msdn.microsoft.com/1d8316d3-83ed-4f8b-bed4-09533d6f3591">GetRawInputDeviceInfo</a> with the <i>hDevice</i> from <a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a>.

Raw input is available only when the application calls <a href="https://msdn.microsoft.com/abf60a07-5d82-4737-96df-b76c9c449261">RegisterRawInputDevices</a> with valid device specifications. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a76d9b93-4faa-43c4-b72e-2ca9fc306703">GetRawInputBuffer</a>



<a href="https://msdn.microsoft.com/a2a15b77-58ef-4632-80dd-2770687c0e0f">GetRawInputData</a>



<a href="https://msdn.microsoft.com/021d4b1a-69a9-482f-a796-21d74a98fbff">RAWHID</a>



<a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/536caca4-9368-486c-9ae4-6778497daf5f">RAWKEYBOARD</a>



<a href="https://msdn.microsoft.com/61925071-06b1-4471-8f34-7f1bd0c17d6d">RAWMOUSE</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

