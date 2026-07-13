---
UID: NS:shlobj_core._FILEGROUPDESCRIPTORA
title: FILEGROUPDESCRIPTORA (shlobj_core.h)
description: Defines the CF_FILEGROUPDESCRIPTOR clipboard format. (ANSI)
helpviewer_keywords: ["*LPFILEGROUPDESCRIPTORA","FILEGROUPDESCRIPTOR","FILEGROUPDESCRIPTOR structure [Windows Shell]","FILEGROUPDESCRIPTORA","FILEGROUPDESCRIPTORW","LPFILEGROUPDESCRIPTOR","LPFILEGROUPDESCRIPTOR structure pointer [Windows Shell]","_FILEGROUPDESCRIPTORA","_FILEGROUPDESCRIPTORW","_win32_FILEGROUPDESCRIPTOR","shell.FILEGROUPDESCRIPTOR","shlobj_core/FILEGROUPDESCRIPTOR","shlobj_core/LPFILEGROUPDESCRIPTOR"]
old-location: shell\FILEGROUPDESCRIPTOR.htm
tech.root: shell
ms.assetid: 9357ab73-086c-44db-8f89-e14240647e89
ms.date: 12/05/2018
ms.keywords: '*LPFILEGROUPDESCRIPTORA, FILEGROUPDESCRIPTOR, FILEGROUPDESCRIPTOR structure [Windows Shell], FILEGROUPDESCRIPTORA, FILEGROUPDESCRIPTORW, LPFILEGROUPDESCRIPTOR, LPFILEGROUPDESCRIPTOR structure pointer [Windows Shell], _FILEGROUPDESCRIPTORA, _FILEGROUPDESCRIPTORW, _win32_FILEGROUPDESCRIPTOR, shell.FILEGROUPDESCRIPTOR, shlobj_core/FILEGROUPDESCRIPTOR, shlobj_core/LPFILEGROUPDESCRIPTOR'
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
targetos: Windows
req.typenames: FILEGROUPDESCRIPTORA, *LPFILEGROUPDESCRIPTORA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILEGROUPDESCRIPTORA
 - shlobj_core/_FILEGROUPDESCRIPTORA
 - LPFILEGROUPDESCRIPTORA
 - shlobj_core/LPFILEGROUPDESCRIPTORA
 - FILEGROUPDESCRIPTORA
 - shlobj_core/FILEGROUPDESCRIPTORA
dev_langs:
 - c++
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
---

# FILEGROUPDESCRIPTORA structure


## -description

Defines the CF_FILEGROUPDESCRIPTOR clipboard format.

## -struct-fields

### -field cItems

Type: <b>UINT</b>

The number of elements in <b>fgd</b>.

### -field fgd

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora">FILEDESCRIPTOR</a>[1]</b>

An array of <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora">FILEDESCRIPTOR</a> structures that contain the file information.

## -remarks

> [!NOTE]
> The shlobj_core.h header defines FILEGROUPDESCRIPTOR as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
