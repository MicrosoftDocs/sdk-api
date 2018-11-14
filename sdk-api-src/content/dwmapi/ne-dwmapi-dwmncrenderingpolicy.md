---
UID: NE:dwmapi.DWMNCRENDERINGPOLICY
title: DWMNCRENDERINGPOLICY
author: windows-sdk-content
description: Flags used by the DwmSetWindowAttribute function to specify the non-client area rendering policy.
old-location: dwm\dwmncrenderingpolicy.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\enums\dwmncrenderingpolicy.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DWMNCRENDERINGPOLICY, DWMNCRENDERINGPOLICY enumeration [Desktop Window Manager], DWMNCRP_DISABLED, DWMNCRP_ENABLED, DWMNCRP_LAST, DWMNCRP_USEWINDOWSTYLE, _udwm_dwmncrenderingpolicy, _udwm_dwmncrenderingpolicy_cpp, dwm.dwmncrenderingpolicy, dwmapi/DWMNCRENDERINGPOLICY, dwmapi/DWMNCRP_DISABLED, dwmapi/DWMNCRP_ENABLED, dwmapi/DWMNCRP_LAST, dwmapi/DWMNCRP_USEWINDOWSTYLE, winui._udwm_dwmncrenderingpolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dwmapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWMNCRENDERINGPOLICY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWMNCRENDERINGPOLICY enumeration


## -description


Flags used by the <a href="https://msdn.microsoft.com/en-us/library/Aa969524(v=VS.85).aspx">DwmSetWindowAttribute</a> function to specify the non-client area rendering policy.


## -enum-fields




### -field DWMNCRP_USEWINDOWSTYLE

The non-client rendering area is rendered based on the window style.


### -field DWMNCRP_DISABLED

The non-client area rendering is disabled; the window style is ignored.


### -field DWMNCRP_ENABLED

The non-client area rendering is enabled; the window style is ignored.


### -field DWMNCRP_LAST

The maximum recognized <a href="https://msdn.microsoft.com/en-us/library/Aa969529(v=VS.85).aspx">DWMNCRENDERINGPOLICY</a> value, used for validation purposes.


## -remarks



To use a <b>DWMNCRENDERINGPOLICY</b> value, set the <i>dwAttribute</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Aa969524(v=VS.85).aspx">DwmSetWindowAttribute</a> function to <b>DWMWA_NCRENDERING_POLICY</b>. Set the <i>pvAttribute</i> parameter to the <b>DWMNCRENDERINGPOLICY</b> value.



