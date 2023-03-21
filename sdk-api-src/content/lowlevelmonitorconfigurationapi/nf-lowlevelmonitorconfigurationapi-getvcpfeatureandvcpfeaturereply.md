---
UID: NF:lowlevelmonitorconfigurationapi.GetVCPFeatureAndVCPFeatureReply
title: GetVCPFeatureAndVCPFeatureReply function (lowlevelmonitorconfigurationapi.h)
description: Retrieves the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.
helpviewer_keywords: ["GetVCPFeatureAndVCPFeatureReply","GetVCPFeatureAndVCPFeatureReply function [Monitor Configuration]","lowlevelmonitorconfigurationapi/GetVCPFeatureAndVCPFeatureReply","monitor.getvcpfeatureandvcpfeaturereply"]
old-location: monitor\getvcpfeatureandvcpfeaturereply.htm
tech.root: Monitor
ms.assetid: b0b06137-8f67-46fc-ba6b-3022f3331fa5
ms.date: 12/05/2018
ms.keywords: GetVCPFeatureAndVCPFeatureReply, GetVCPFeatureAndVCPFeatureReply function [Monitor Configuration], lowlevelmonitorconfigurationapi/GetVCPFeatureAndVCPFeatureReply, monitor.getvcpfeatureandvcpfeaturereply
req.header: lowlevelmonitorconfigurationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetVCPFeatureAndVCPFeatureReply
 - lowlevelmonitorconfigurationapi/GetVCPFeatureAndVCPFeatureReply
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetVCPFeatureAndVCPFeatureReply
---

# GetVCPFeatureAndVCPFeatureReply function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param bVCPCode [in]

VCP code to query. The VCP codes are Include the VESA Monitor Control Command Set (MCCS) standard, versions 1.0 and 2.0. This parameter must specify a continuous or non-continuous VCP, or a vendor-specific code. It should not be a table control code.

### -param pvct [out]

Receives the VCP code type, as a member of the <a href="/windows/win32/api/lowlevelmonitorconfigurationapi/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type">MC_VCP_CODE_TYPE</a> enumeration. This parameter can be <b>NULL</b>.

### -param pdwCurrentValue [out]

Receives the current value of the VCP code. This parameter can be <b>NULL</b>.

### -param pdwMaximumValue [out]

If <i>bVCPCode</i> specifies a continuous VCP code, this parameter receives the maximum value of the VCP code. If <i>bVCPCode</i> specifies a non-continuous VCP code, the value received in this parameter is undefined. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function corresponds to the "Get VCP Feature &amp; VCP Feature Reply" command from the Display Data Channel Command Interface (DDC/CI) standard. Vendor-specific VCP codes can be used with this function.
      

This function takes about 40 milliseconds to return.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>