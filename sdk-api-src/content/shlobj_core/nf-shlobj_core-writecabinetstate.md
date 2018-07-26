---
UID: NF:shlobj_core.WriteCabinetState
title: WriteCabinetState function
author: windows-sdk-content
description: WriteCabinetState may be altered or unavailable.
old-location: shell\WriteCabinetState.htm
old-project: shell
ms.assetid: cbd08812-eedc-4ba7-827e-1e5d1e3e6368
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: WriteCabinetState, WriteCabinetState function [Windows Shell], _win32_WriteCabinetState, shell.WriteCabinetState, shlobj_core/WriteCabinetState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - WriteCabinetState
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# WriteCabinetState function


## -description


<p class="CCE_Message">[<b>WriteCabinetState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Writes the information contained in a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure into the registry.


## -parameters




### -param pcs [in]

Type: <b><a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure that holds the values to be set.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.



