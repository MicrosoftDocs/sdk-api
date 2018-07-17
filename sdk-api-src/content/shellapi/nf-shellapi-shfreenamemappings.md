---
UID: NF:shellapi.SHFreeNameMappings
title: SHFreeNameMappings function
author: windows-sdk-content
description: Frees a file name mapping object that was retrieved by the SHFileOperation function.
old-location: shell\SHFreeNameMappings.htm
old-project: shell
ms.assetid: 4552b2e0-9257-48f8-84cc-003217f1696f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHFreeNameMappings, SHFreeNameMappings function [Windows Shell], _win32_SHFreeNameMappings, shell.SHFreeNameMappings, shellapi/SHFreeNameMappings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHFreeNameMappings
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHFreeNameMappings function


## -description


Frees a file name mapping object that was retrieved by the <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.


## -parameters




### -param hNameMappings [in, optional]

Type: <b>HANDLE</b>

A handle to the file name mapping object to be freed.


## -returns



This function does not return a value.



