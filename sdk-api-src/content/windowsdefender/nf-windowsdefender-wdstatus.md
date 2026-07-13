---
UID: NF:windowsdefender.WDStatus
title: WDStatus function (windowsdefender.h)
description: Returns the current status of Windows Defender.
helpviewer_keywords: ["WDStatus","WDStatus function [Legacy Windows Environment Features]","lwef.defender_wdstatus","shell.defender_wdstatus","shell_defender_WDStatus","windowsdefender/WDStatus"]
old-location: lwef\defender_wdstatus.htm
tech.root: lwef
ms.assetid: 885729a7-13a4-401e-ad7b-4f679777531b
ms.date: 12/05/2018
ms.keywords: WDStatus, WDStatus function [Legacy Windows Environment Features], lwef.defender_wdstatus, shell.defender_wdstatus, shell_defender_WDStatus, windowsdefender/WDStatus
req.header: windowsdefender.h
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
req.dll: MpClient.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WDStatus
 - windowsdefender/WDStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MpClient.dll
api_name:
 - WDStatus
---

# WDStatus function


## -description

Returns the current status of Windows Defender.

## -parameters

### -param pfEnabled [out]

Type: <b>BOOL*</b>

The status of Windows Defender as a boolean. <b>TRUE</b> means Windows Defender is in enabled status. <b>FALSE</b> means Windows Defender is in disabled status.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windowsdefender/nf-windowsdefender-wdenable">WDEnable</a>