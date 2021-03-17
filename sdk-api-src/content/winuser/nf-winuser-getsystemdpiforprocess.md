---
UID: NF:winuser.GetSystemDpiForProcess
title: GetSystemDpiForProcess function (winuser.h)
description: Retrieves the system DPI associated with a given process. This is useful for avoiding compatibility issues that arise from sharing DPI-sensitive information between multiple system-aware processes with different system DPI values.
helpviewer_keywords: ["GetSystemDpiForProcess","GetSystemDpiForProcess function [High DPI]","hidpi.getsystemdpiforprocess","winuser/GetSystemDpiForProcess"]
old-location: hidpi\getsystemdpiforprocess.htm
tech.root: hidpi
ms.assetid: 94236ECF-E69A-4D77-AABA-D43FE8DF8203
ms.date: 12/05/2018
ms.keywords: GetSystemDpiForProcess, GetSystemDpiForProcess function [High DPI], hidpi.getsystemdpiforprocess, winuser/GetSystemDpiForProcess
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemDpiForProcess
 - winuser/GetSystemDpiForProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetSystemDpiForProcess
---

# GetSystemDpiForProcess function


## -description

Retrieves the system DPI associated with a given process. This is useful for avoiding compatibility issues that arise from sharing DPI-sensitive information between multiple system-aware processes with different system DPI values.

## -parameters

### -param hProcess

The handle for the process to examine. If this value is null, this API behaves identically to <a href="/windows/desktop/api/winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a>.

## -returns

The process's system DPI value.

## -remarks

The return value will be dependent based upon the process passed as a parameter. If the specified process has a <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> value of <b>DPI_AWARENESS_UNAWARE</b>, the return value will be 96. That is because the current context always assumes a DPI of 96. For any other <b>DPI_AWARENESS</b> value, the return value will be the actual system DPI of the given process.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a>