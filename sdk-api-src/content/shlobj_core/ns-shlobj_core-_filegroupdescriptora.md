---
UID: NS:shlobj_core._FILEGROUPDESCRIPTORA
title: "_FILEGROUPDESCRIPTORA"
author: windows-sdk-content
description: Defines the CF_FILEGROUPDESCRIPTOR clipboard format.
old-location: shell\FILEGROUPDESCRIPTOR.htm
tech.root: shell
ms.assetid: 9357ab73-086c-44db-8f89-e14240647e89
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPFILEGROUPDESCRIPTORA, FILEGROUPDESCRIPTOR, FILEGROUPDESCRIPTOR structure [Windows Shell], FILEGROUPDESCRIPTORA, LPFILEGROUPDESCRIPTOR, LPFILEGROUPDESCRIPTOR structure pointer [Windows Shell], _FILEGROUPDESCRIPTORA, _FILEGROUPDESCRIPTORW, _win32_FILEGROUPDESCRIPTOR, shell.FILEGROUPDESCRIPTOR, shlobj_core/FILEGROUPDESCRIPTOR, shlobj_core/LPFILEGROUPDESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shlobj_core.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj_core.h
api_name:
 - FILEGROUPDESCRIPTOR
product: Windows
targetos: Windows
req.typenames: FILEGROUPDESCRIPTORA, *LPFILEGROUPDESCRIPTORA
req.redist: 
---

# _FILEGROUPDESCRIPTORA structure


## -description


Defines the CF_FILEGROUPDESCRIPTOR clipboard format.


## -struct-fields




### -field cItems

Type: <b>UINT</b>

The number of elements in <b>fgd</b>.


### -field fgd

Type: <b><a href="https://msdn.microsoft.com/b81a7e52-5bd8-4fa4-bd76-9a58afaceec0">FILEDESCRIPTOR</a>[1]</b>

An array of <a href="https://msdn.microsoft.com/b81a7e52-5bd8-4fa4-bd76-9a58afaceec0">FILEDESCRIPTOR</a> structures that contain the file information.

