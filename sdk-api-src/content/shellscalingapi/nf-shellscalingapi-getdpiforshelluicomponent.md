---
UID: NF:shellscalingapi.GetDpiForShellUIComponent
title: GetDpiForShellUIComponent function
author: windows-sdk-content
description: Retrieves the dots per inch (dpi) occupied by a SHELL_UI_COMPONENT based on the current scale factor and PROCESS_DPI_AWARENESS.
old-location: shell\getdpiforshelluicomponent.htm
tech.root: shell
ms.assetid: D5198497-DBD5-439E-809C-A36211C2774C
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetDpiForShellUIComponent, GetDpiForShellUiComponent, GetDpiForShellUiComponent function [Windows Shell], shell.getdpiforshelluicomponent, shellscalingapi/GetDpiForShellUiComponent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDpiForShellUIComponent function


## -description


Retrieves the dots per inch (dpi) occupied by a <a href="https://msdn.microsoft.com/40919C36-228A-4909-A517-8B152BE47D36">SHELL_UI_COMPONENT</a> based on the current scale factor and <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>.


## -parameters




### -param Arg1 [in]

The type of shell component.


## -returns



The DPI required for an icon of this type.



