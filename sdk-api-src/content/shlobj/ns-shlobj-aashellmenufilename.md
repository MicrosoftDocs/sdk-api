---
UID: NS:shlobj.tagAAMENUFILENAME
title: AASHELLMENUFILENAME (shlobj.h)
description: A variable-size structure that contains information about a menu file name.
helpviewer_keywords: ["*LPAASHELLMENUFILENAME","AASHELLMENUFILENAME","AASHELLMENUFILENAME structure [Windows Shell]","LPAASHELLMENUFILENAME","LPAASHELLMENUFILENAME structure pointer [Windows Shell]","_win32_AASHELLMENUFILENAME_str","shell.AASHELLMENUFILENAME_str","shlobj/AASHELLMENUFILENAME","shlobj/LPAASHELLMENUFILENAME"]
old-location: shell\AASHELLMENUFILENAME_str.htm
tech.root: shell
ms.assetid: f84e837f-61b0-4df4-9ff7-dc2d3d898d99
ms.date: 12/05/2018
ms.keywords: '*LPAASHELLMENUFILENAME, AASHELLMENUFILENAME, AASHELLMENUFILENAME structure [Windows Shell], LPAASHELLMENUFILENAME, LPAASHELLMENUFILENAME structure pointer [Windows Shell], _win32_AASHELLMENUFILENAME_str, shell.AASHELLMENUFILENAME_str, shlobj/AASHELLMENUFILENAME, shlobj/LPAASHELLMENUFILENAME'
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: AASHELLMENUFILENAME, *LPAASHELLMENUFILENAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAAMENUFILENAME
 - shlobj/tagAAMENUFILENAME
 - LPAASHELLMENUFILENAME
 - shlobj/LPAASHELLMENUFILENAME
 - AASHELLMENUFILENAME
 - shlobj/AASHELLMENUFILENAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - AASHELLMENUFILENAME
---

# AASHELLMENUFILENAME structure


## -description

A variable-size structure that contains information about a menu file name.

## -struct-fields

### -field cbTotal

Type: <b>SHORT</b>

The size of the structure, in bytes.

### -field rgbReserved

Type: <b>BYTE[12]</b>

Reserved. Applications should ignore this value.

### -field szFileName

Type: <b>TCHAR[1]</b>

The menu file name. This string is in Unicode on Windows 2000.

## -remarks

<div class="alert"><b>Important</b>  This structure cannot be used with operating systems later than Windows 2000.</div>
<div> </div>
When reading an <b>AASHELLMENUFILENAME</b> structure, first read a single SHORT to determine the total size of the structure, then use that value to read the remainder of the structure.

## -see-also

<a href="/windows/desktop/api/shlobj/ns-shlobj-aashellmenuitem">AASHELLMENUITEM</a>