---
UID: NF:winuser.DisplayConfigSetDeviceInfo
title: DisplayConfigSetDeviceInfo function (winuser.h)
description: The DisplayConfigSetDeviceInfo function sets the properties of a target.
helpviewer_keywords: ["CCD_Functions_0124386b-2a62-4d91-9eca-9268a569c976.xml","DisplayConfigSetDeviceInfo","DisplayConfigSetDeviceInfo function [Display Devices]","display.displayconfigsetdeviceinfo","winuser/DisplayConfigSetDeviceInfo"]
old-location: display\displayconfigsetdeviceinfo.htm
tech.root: display
ms.assetid: 4050b1f0-a588-427c-a0df-eefdc488fc20
ms.date: 12/05/2018
ms.keywords: CCD_Functions_0124386b-2a62-4d91-9eca-9268a569c976.xml, DisplayConfigSetDeviceInfo, DisplayConfigSetDeviceInfo function [Display Devices], display.displayconfigsetdeviceinfo, winuser/DisplayConfigSetDeviceInfo
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
req.lib: User32.lib; OneCoreUAP.lib on Windows 10
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DisplayConfigSetDeviceInfo
 - winuser/DisplayConfigSetDeviceInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-SysParams-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-SysParams-l1-1-0.dll
api_name:
 - DisplayConfigSetDeviceInfo
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# DisplayConfigSetDeviceInfo function


## -description

The <b>DisplayConfigSetDeviceInfo</b> function sets the properties of a target.

## -parameters

### -param setPacket [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information to set for the device. The type and size of additional data that <b>DisplayConfigSetDeviceInfo</b> uses for the configuration comes after the header structure. This additional data depends on the packet type, as specified by the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER. For example, if the caller wants to change the boot persistence, that caller allocates and fills a <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_set_target_persistence">DISPLAYCONFIG_SET_TARGET_PERSISTENCE</a> structure and passes a pointer to this structure in <i>setPacket</i>. Note that the first member of the DISPLAYCONFIG_SET_TARGET_PERSISTENCE structure is the DISPLAYCONFIG_DEVICE_INFO_HEADER.

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
The system is not running a graphics driver that was written according to the <a href="/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide">Windows Display Driver Model (WDDM)</a>. The function is only supported on a system with a WDDM driver running.

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
The size of the packet that the caller passes is not big enough.

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

<b>DisplayConfigSetDeviceInfo</b> can currently only be used to start and stop boot persisted force projection on an analog target. For more information about boot persistence, see <a href="/windows-hardware/drivers/display/forced-versus-connected-targets">Forced Versus Connected Targets</a>.

<b>DisplayConfigSetDeviceInfo</b> can only be used to set DISPLAYCONFIG_DEVICE_INFO_SET_XXX type of information. <b>DisplayConfigSetDeviceInfo</b> fails if the <b>type</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> is set to one of the DISPLAYCONFIG_DEVICE_INFO_GET_XXX values.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>
