---
UID: NF:winuser.DisplayConfigGetDeviceInfo
title: DisplayConfigGetDeviceInfo function
author: windows-driver-content
description: The DisplayConfigGetDeviceInfo function retrieves display configuration information about the device.
old-location: display\displayconfiggetdeviceinfo.htm
old-project: display
ms.assetid: 249dcb1a-4ce3-4478-8331-fb81e91313b0
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: CCD_Functions_e8c6c762-da08-4b21-b016-e66bb44c248d.xml, DisplayConfigGetDeviceInfo, DisplayConfigGetDeviceInfo function [Display Devices], display.displayconfiggetdeviceinfo, winuser/DisplayConfigGetDeviceInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	API-MS-Win-NTUser-SysParams-l1-1-0.dll
-	MinUser.dll
-	Ext-MS-Win-RTCore-NTUser-SysParams-l1-1-0.dll
api_name:
-	DisplayConfigGetDeviceInfo
product: Windows
targetos: Windows
req.lib: User32.lib; OneCoreUAP.lib on Windows 10
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DisplayConfigGetDeviceInfo function


## -description


The <b>DisplayConfigGetDeviceInfo</b> function retrieves display configuration information about the device.


## -parameters




### -param requestPacket [in, out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure. This structure contains information about the request, which includes the packet type in the <b>type</b> member. The type and size of additional data that <b>DisplayConfigGetDeviceInfo</b> returns after the header structure depend on the packet type. 


## -returns



The function returns one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The combination of parameters and flags specified are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The system is not running a graphics driver that was written according to the <a href="https://msdn.microsoft.com/d9dc0d48-aea4-4614-a23b-e2449800469f">Windows Display Driver Model (WDDM)</a>. The function is only supported on a system with a WDDM driver running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the console session. This error occurs if the calling process does not have access to the current desktop or is running on a remote session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the packet that the caller passes is not big enough for the information that the caller requests.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



Use the <b>DisplayConfigGetDeviceInfo</b>function to obtain additional information about a source or target for an adapter, such as the display name, the preferred display mode, and source device name.

The caller can call <b>DisplayConfigGetDeviceInfo</b>to obtain more friendly names to display in the user interface. The caller can obtain names for the adapter, the source, and the target. The caller can also call <b>DisplayConfigGetDeviceInfo</b>to obtain the best resolution of the connected display device. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553989">DISPLAYCONFIG_TARGET_DEVICE_NAME</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553990">DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553909">DisplayConfigSetDeviceInfo</a>
 

 

