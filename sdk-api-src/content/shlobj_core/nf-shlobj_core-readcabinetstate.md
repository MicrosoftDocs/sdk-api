---
UID: NF:shlobj_core.ReadCabinetState
title: ReadCabinetState function
author: windows-sdk-content
description: ReadCabinetState may be altered or unavailable.
old-location: shell\ReadCabinetState.htm
old-project: shell
ms.assetid: 0f0c6a10-588f-4c79-b73b-cf0bf9336ffc
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ReadCabinetState, ReadCabinetState function [Windows Shell], _win32_ReadCabinetState, shell.ReadCabinetState, shlobj_core/ReadCabinetState
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	ReadCabinetState
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ReadCabinetState function


## -description


<p class="CCE_Message">[<b>ReadCabinetState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Fills a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure with information from the registry.


## -parameters




### -param pcs [out]

Type: <b><a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a>*</b>

When this function returns, contains a pointer to a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure that contains either information pulled from the registry or default information.


### -param cLength [in]

Type: <b>int</b>

The size of the structure pointed to by <i>pcs</i>, in bytes.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the returned structure contains information from the registry. Returns <b>FALSE</b> if the structure contains default information.



