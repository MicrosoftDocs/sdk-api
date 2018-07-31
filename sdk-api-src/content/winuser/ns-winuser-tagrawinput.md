---
UID: NS:winuser.tagRAWINPUT
title: tagRAWINPUT
author: windows-sdk-content
description: Contains the raw input from a device.
old-location: inputdev\rawinput.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinput.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms645571(v=VS.85).aspx">RAWINPUTHEADER</a></b>

The raw input data. 


### -field data


### -field data.mouse

<b>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms645578(v=VS.85).aspx">RAWMOUSE</a></b>
</b>
If the data comes from a mouse, this is the raw input data. 


### -field data.keyboard

<b>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms645575(v=VS.85).aspx">RAWKEYBOARD</a></b>
</b>
If the data comes from a keyboard, this is the raw input data. 


### -field data.hid

<b>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms645549(v=VS.85).aspx">RAWHID</a></b>
</b>
If the data comes from an HID, this is the raw input data. 


## -remarks



The handle to this structure is passed in the <i>lParam</i> parameter of <a href="https://msdn.microsoft.com/en-us/library/ms645590(v=VS.85).aspx">WM_INPUT</a>.

To get detailed information -- such as the header and the content of the raw input -- call <a href="https://msdn.microsoft.com/en-us/library/ms645596(v=VS.85).aspx">GetRawInputData</a>.

To read the <b>RAWINPUT</b> in the message loop as a buffered read, call <a href="https://msdn.microsoft.com/en-us/library/ms645595(v=VS.85).aspx">GetRawInputBuffer</a>. 

To get device specific information, call <a href="https://msdn.microsoft.com/en-us/library/ms645597(v=VS.85).aspx">GetRawInputDeviceInfo</a> with the <i>hDevice</i> from <a href="https://msdn.microsoft.com/en-us/library/ms645571(v=VS.85).aspx">RAWINPUTHEADER</a>.

Raw input is available only when the application calls <a href="https://msdn.microsoft.com/en-us/library/ms645600(v=VS.85).aspx">RegisterRawInputDevices</a> with valid device specifications. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645595(v=VS.85).aspx">GetRawInputBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645596(v=VS.85).aspx">GetRawInputData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645549(v=VS.85).aspx">RAWHID</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645571(v=VS.85).aspx">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645575(v=VS.85).aspx">RAWKEYBOARD</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645578(v=VS.85).aspx">RAWMOUSE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

