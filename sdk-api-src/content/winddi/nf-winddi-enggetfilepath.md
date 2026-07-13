---
UID: NF:winddi.EngGetFilePath
title: EngGetFilePath function (winddi.h)
description: The EngGetFilePath function determines the file path associated with the specified font file.
helpviewer_keywords: ["EngGetFilePath","EngGetFilePath function [Display Devices]","display.enggetfilepath","gdifncs_219a84bc-93a3-4a5f-bf0e-d0087737fdb0.xml","winddi/EngGetFilePath"]
old-location: display\enggetfilepath.htm
tech.root: display
ms.assetid: 751a9bef-f1ee-43a0-958b-f90ac63b2f37
ms.date: 12/05/2018
ms.keywords: EngGetFilePath, EngGetFilePath function [Display Devices], display.enggetfilepath, gdifncs_219a84bc-93a3-4a5f-bf0e-d0087737fdb0.xml, winddi/EngGetFilePath
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngGetFilePath
 - winddi/EngGetFilePath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngGetFilePath
---

# EngGetFilePath function


## -description

The <b>EngGetFilePath</b> function determines the file path associated with the specified font file.

## -parameters

### -param h [in]

Handle to the font file.

### -param pDest [out]

Pointer to a buffer that will contain the fully qualified path of the directory containing the font file. The buffer can contain at most MAX_PATH + 1 characters, including the terminating null character. The constant MAX_PATH is defined in <i>windef.h</i>.

## -returns

<b>EngGetFilePath</b> returns <b>TRUE</b> if it succeeds in obtaining the file path of the font file. Otherwise, <b>EngGetFilePath</b> returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmapfontfilefd">EngMapFontFileFD</a>