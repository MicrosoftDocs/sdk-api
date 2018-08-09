---
UID: NS:winuser.tagRAWINPUTDEVICELIST
title: tagRAWINPUTDEVICELIST
author: windows-sdk-content
description: Contains information about a raw input device.
old-location: inputdev\rawinputdevicelist.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawinputdevicelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PRAWINPUTDEVICELIST, PRAWINPUTDEVICELIST, PRAWINPUTDEVICELIST structure pointer [Keyboard and Mouse Input], RAWINPUTDEVICELIST, RAWINPUTDEVICELIST structure [Keyboard and Mouse Input], RIM_TYPEHID, RIM_TYPEKEYBOARD, RIM_TYPEMOUSE, _win32_RAWINPUTDEVICELIST_str, _win32_rawinputdevicelist_str_cpp, inputdev.rawinputdevicelist, tagRAWINPUTDEVICELIST, winui._win32_rawinputdevicelist_str, winuser/PRAWINPUTDEVICELIST, winuser/RAWINPUTDEVICELIST"
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
req.typenames: RAWINPUTDEVICELIST, *PRAWINPUTDEVICELIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWINPUTDEVICELIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagRAWINPUTDEVICELIST structure


## -description


Contains information about a raw input device.


## -struct-fields




### -field hDevice

Type: <b>HANDLE</b>

A handle to the raw input device. 


### -field dwType

Type: <b>DWORD</b>

The type of device. This can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEHID"></a><a id="rim_typehid"></a><dl>
<dt><b>RIM_TYPEHID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The device is an HID that is not a keyboard and not a mouse.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEKEYBOARD"></a><a id="rim_typekeyboard"></a><dl>
<dt><b>RIM_TYPEKEYBOARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The device is a keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="RIM_TYPEMOUSE"></a><a id="rim_typemouse"></a><dl>
<dt><b>RIM_TYPEMOUSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The device is a mouse.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645598(v=VS.85).aspx">GetRawInputDeviceList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

