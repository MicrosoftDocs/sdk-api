---
UID: NS:winuser.tagRID_DEVICE_INFO_HID
title: tagRID_DEVICE_INFO_HID
author: windows-sdk-content
description: Defines the raw input data coming from the specified Human Interface Device (HID).
old-location: inputdev\rid_device_info_hid.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rid_device_info_hid.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*PRID_DEVICE_INFO_HID, PRID_DEVICE_INFO_HID, PRID_DEVICE_INFO_HID structure pointer [Keyboard and Mouse Input], RID_DEVICE_INFO_HID, RID_DEVICE_INFO_HID structure [Keyboard and Mouse Input], _win32_RID_DEVICE_INFO_HID_str, _win32_rid_device_info_hid_str_cpp, inputdev.rid_device_info_hid, tagRID_DEVICE_INFO_HID, winui._win32_rid_device_info_hid_str, winuser/PRID_DEVICE_INFO_HID, winuser/RID_DEVICE_INFO_HID"
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
 - RID_DEVICE_INFO_HID
product: Windows
targetos: Windows
req.typenames: RID_DEVICE_INFO_HID, *PRID_DEVICE_INFO_HID
req.redist: 
---

# tagRID_DEVICE_INFO_HID structure


## -description


Defines the raw input data coming from the specified Human Interface Device (HID). 


## -struct-fields




### -field dwVendorId

Type: <b>DWORD</b>

The vendor identifier for the HID. 


### -field dwProductId

Type: <b>DWORD</b>

The product identifier for the HID. 


### -field dwVersionNumber

Type: <b>DWORD</b>

The version number for the HID. 


### -field usUsagePage

Type: <b>USHORT</b>

The top-level collection Usage Page for the device. 


### -field usUsage

Type: <b>USHORT</b>

The top-level collection Usage for the device. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645581(v=VS.85).aspx">RID_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

