---
UID: NF:shellscalingapi.GetDpiForShellUIComponent
title: GetDpiForShellUIComponent function (shellscalingapi.h)
description: Retrieves the dots per inch (dpi) occupied by a SHELL_UI_COMPONENT based on the current scale factor and PROCESS_DPI_AWARENESS.
old-location: shell\getdpiforshelluicomponent.htm
tech.root: shell
ms.assetid: D5198497-DBD5-439E-809C-A36211C2774C
ms.date: 12/05/2018
ms.keywords: GetDpiForShellUIComponent, GetDpiForShellUiComponent, GetDpiForShellUiComponent function [Windows Shell], shell.getdpiforshelluicomponent, shellscalingapi/GetDpiForShellUiComponent
ms.topic: function
f1_keywords:
- shellscalingapi/GetDpiForShellUiComponent
dev_langs:
- c++
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- shcore.dll
- api-ms-win-shcore-scaling-l1-1-1.dll
api_name:
- GetDpiForShellUiComponent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDpiForShellUIComponent function


## -description


Retrieves the dots per inch (dpi) occupied by a <a href="https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-shell_ui_component">SHELL_UI_COMPONENT</a> based on the current scale factor and <a href="https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>.


## -parameters




### -param Arg1 [in]

The type of shell component.


## -returns



The DPI required for an icon of this type.



