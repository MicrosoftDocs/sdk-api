---
UID: NF:dwmapi.DwmEnableMMCSS
title: DwmEnableMMCSS function
author: windows-sdk-content
description: Notifies the Desktop Window Manager (DWM) to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.
old-location: dwm\dwmenablemmcss.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmenablemmcss.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DwmEnableMMCSS, DwmEnableMMCSS function [Desktop Window Manager], _udwm_dwmenablemmcss, _udwm_dwmenablemmcss_cpp, dwm.dwmenablemmcss, dwmapi/DwmEnableMMCSS, winui._udwm_dwmenablemmcss
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - DComp.dll
api_name:
 - DwmEnableMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DwmEnableMMCSS function


## -description


Notifies the Desktop Window Manager (DWM) to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.


## -parameters




### -param fEnableMMCSS

<b>TRUE</b> to instruct DWM to participate in MMCSS scheduling; <b>FALSE</b> to opt out or end participation in MMCSS scheduling.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



DWM will be scheduled by the MMCSS as long as any process that called <b>DwmEnableMMCSS</b> to enable MMCSS is active and has not previously called <b>DwmEnableMMCSS</b> to disable MMCSS.



