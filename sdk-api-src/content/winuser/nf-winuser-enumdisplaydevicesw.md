---
UID: NF:winuser.EnumDisplayDevicesW
title: EnumDisplayDevicesW function
author: windows-sdk-content
description: The EnumDisplayDevices function lets you obtain information about the display devices in the current session.
old-location: gdi\enumdisplaydevices.htm
tech.root: gdi
ms.assetid: df3b493c-23d2-4996-9b79-86009efe3078
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumDisplayDevices, EnumDisplayDevices function [Windows GDI], EnumDisplayDevicesA, EnumDisplayDevicesW, _win32_EnumDisplayDevices, gdi.enumdisplaydevices, winuser/EnumDisplayDevices, winuser/EnumDisplayDevicesA, winuser/EnumDisplayDevicesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDisplayDevicesW (Unicode) and EnumDisplayDevicesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-sysparams-l1-1-0.dll
api_name:
 - EnumDisplayDevices
 - EnumDisplayDevicesA
 - EnumDisplayDevicesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumDisplayDevicesW function


## -description


The <b>EnumDisplayDevices</b> function lets you obtain information about the display devices in the current session.


## -parameters




### -param lpDevice [in]

A pointer to the device name. If <b>NULL</b>, function returns information for the display adapter(s) on the machine, based on <i>iDevNum</i>.

For more information, see Remarks.


### -param iDevNum [in]

An index value that specifies the display device of interest.

The operating system identifies each display device in the current session with an index value. The index values are consecutive integers, starting at 0. If the current session has three display devices, for example, they are specified by the index values 0, 1, and 2.


### -param lpDisplayDevice [out]

A pointer to a <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a> structure that receives information about the display device specified by <i>iDevNum</i>. 

Before calling <b>EnumDisplayDevices</b>, you must initialize the <b>cb</b> member of <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a> to the size, in bytes, of <b>DISPLAY_DEVICE</b>.


### -param dwFlags [in]

Set this flag to EDD_GET_DEVICE_INTERFACE_NAME (0x00000001) to retrieve the device interface name for GUID_DEVINTERFACE_MONITOR, which is registered by the operating system on a per monitor basis. The value is placed in the DeviceID member of the <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a> structure returned in <i>lpDisplayDevice</i>. The resulting device interface name can be used with <a href="SetupAPI_f2cd3b48-9270-4139-94c3-b1d3fc925716.xml">SetupAPI functions</a> and serves as a link between GDI monitor devices and SetupAPI monitor devices. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function fails if <i>iDevNum</i> is greater than the largest device index.




## -remarks



To query all display devices in the current session, call this function in a loop, starting with <i>iDevNum</i> set to 0, and incrementing <i>iDevNum</i> until the function fails. To select all display devices in the desktop, use only the display devices that have the DISPLAY_DEVICE_ATTACHED_TO_DESKTOP flag in the <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a> structure.

To get information on the display adapter, call <b>EnumDisplayDevices</b> with <i>lpDevice</i> set to <b>NULL</b>. For example, <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a>.<b>DeviceString</b> contains the adapter name.

To obtain information on a display monitor, first call <b>EnumDisplayDevices</b> with <i>lpDevice</i> set to <b>NULL</b>. Then call <b>EnumDisplayDevices</b> with <i>lpDevice</i> set to <a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a>.<b>DeviceName</b> from the first call to <b>EnumDisplayDevices</b> and with <i>iDevNum</i> set to zero. Then <b>DISPLAY_DEVICE</b>.<b>DeviceString</b> is the monitor name.

To query all monitor devices associated with an adapter, call <b>EnumDisplayDevices</b> in a loop with <i>lpDevice</i> set to the adapter name, <i>iDevNum</i> set to start at 0, and <i>iDevNum</i> set to increment until the function fails. Note that <b>DISPLAY_DEVICE.DeviceName</b> changes with each call for monitor information, so you must save the adapter name. The function fails when there are no more monitors for the adapter.




## -see-also




<a href="https://msdn.microsoft.com/208bf1cc-c03c-4d03-92e4-32fcf856b4d8">ChangeDisplaySettings</a>



<a href="https://msdn.microsoft.com/1448e04c-1452-4eab-bda4-4d249cb67a24">ChangeDisplaySettingsEx</a>



<a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>



<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/9a7813fe-358a-44eb-99da-c63f98d055c3">DISPLAY_DEVICE</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/af73610b-bcd8-4660-800e-84fa0cc5b4eb">EnumDisplaySettings</a>
 

 

