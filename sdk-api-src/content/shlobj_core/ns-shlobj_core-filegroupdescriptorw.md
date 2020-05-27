---
UID: NS:shlobj_core._FILEGROUPDESCRIPTORW
title: FILEGROUPDESCRIPTORW (shlobj_core.h)
description: Defines the CF_FILEGROUPDESCRIPTOR clipboard format.
helpviewer_keywords: ["*LPFILEGROUPDESCRIPTORW","FILEGROUPDESCRIPTOR","FILEGROUPDESCRIPTOR structure [Windows Shell]","FILEGROUPDESCRIPTORA","FILEGROUPDESCRIPTORW","LPFILEGROUPDESCRIPTOR","LPFILEGROUPDESCRIPTOR structure pointer [Windows Shell]","_FILEGROUPDESCRIPTORA","_FILEGROUPDESCRIPTORW","_win32_FILEGROUPDESCRIPTOR","shell.FILEGROUPDESCRIPTOR","shlobj_core/FILEGROUPDESCRIPTOR","shlobj_core/LPFILEGROUPDESCRIPTOR"]
old-location: shell\FILEGROUPDESCRIPTOR.htm
tech.root: shell
ms.assetid: 9357ab73-086c-44db-8f89-e14240647e89
ms.date: 12/05/2018
ms.keywords: '*LPFILEGROUPDESCRIPTORW, FILEGROUPDESCRIPTOR, FILEGROUPDESCRIPTOR structure [Windows Shell], FILEGROUPDESCRIPTORA, FILEGROUPDESCRIPTORW, LPFILEGROUPDESCRIPTOR, LPFILEGROUPDESCRIPTOR structure pointer [Windows Shell], _FILEGROUPDESCRIPTORA, _FILEGROUPDESCRIPTORW, _win32_FILEGROUPDESCRIPTOR, shell.FILEGROUPDESCRIPTOR, shlobj_core/FILEGROUPDESCRIPTOR, shlobj_core/LPFILEGROUPDESCRIPTOR'
f1_keywords:
- shlobj_core/FILEGROUPDESCRIPTOR
dev_langs:
- c++
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
- FILEGROUPDESCRIPTORA
- FILEGROUPDESCRIPTORW
targetos: Windows
req.typenames: FILEGROUPDESCRIPTORW, *LPFILEGROUPDESCRIPTORW
req.redist: 
ms.custom: 19H1
---

# FILEGROUPDESCRIPTORW structure


## -description


Defines the CF_FILEGROUPDESCRIPTOR clipboard format.


## -struct-fields




### -field cItems

Type: <b>UINT</b>

The number of elements in <b>fgd</b>.


### -field fgd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora">FILEDESCRIPTOR</a>[1]</b>

An array of <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora">FILEDESCRIPTOR</a> structures that contain the file information.

