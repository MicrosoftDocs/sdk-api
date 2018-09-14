---
UID: NS:winuser.tagRID_DEVICE_INFO_MOUSE
title: tagRID_DEVICE_INFO_MOUSE
author: windows-sdk-content
description: Defines the raw input data coming from the specified mouse.
old-location: inputdev\rid_device_info_mouse.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rid_device_info_mouse.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PRID_DEVICE_INFO_MOUSE, PRID_DEVICE_INFO_MOUSE, PRID_DEVICE_INFO_MOUSE structure pointer [Keyboard and Mouse Input], RID_DEVICE_INFO_MOUSE, RID_DEVICE_INFO_MOUSE structure [Keyboard and Mouse Input], _win32_RID_DEVICE_INFO_MOUSE_str, _win32_rid_device_info_mouse_str_cpp, inputdev.rid_device_info_mouse, tagRID_DEVICE_INFO_MOUSE, winui._win32_rid_device_info_mouse_str, winuser/PRID_DEVICE_INFO_MOUSE, winuser/RID_DEVICE_INFO_MOUSE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RID_DEVICE_INFO_MOUSE
product: Windows
targetos: Windows
req.typenames: RID_DEVICE_INFO_MOUSE, *PRID_DEVICE_INFO_MOUSE
req.redist: 
---

# tagRID_DEVICE_INFO_MOUSE structure


## -description


Defines the raw input data coming from the specified mouse.


## -struct-fields




### -field dwId

Type: <b>DWORD</b>

The identifier of the mouse device.


### -field dwNumberOfButtons

Type: <b>DWORD</b>

The number of buttons for the mouse.


### -field dwSampleRate

Type: <b>DWORD</b>

The number of data points per second. This information may not be applicable for every mouse device.


### -field fHasHorizontalWheel

Type: <b>BOOL</b>

<b>TRUE</b> if the mouse has a wheel for horizontal scrolling; otherwise, <b>FALSE</b>.
                

<b>Windows XP:  </b>This member is only supported starting with Windows Vista.


## -remarks



For the mouse, the Usage Page is 1 and the Usage is 2.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1d44f5b1-2dbb-4a49-b8c0-8f65bb3fa79a">RID_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

