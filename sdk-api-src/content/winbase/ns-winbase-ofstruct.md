---
UID: NS:winbase._OFSTRUCT
title: OFSTRUCT (winbase.h)
description: Contains information about a file that the OpenFile function opened or attempted to open.
helpviewer_keywords: ["*LPOFSTRUCT","*POFSTRUCT","OFSTRUCT","OFSTRUCT structure [Files]","POFSTRUCT","POFSTRUCT structure pointer [Files]","_OFSTRUCT","_win32_ofstruct_str","base.ofstruct_str","fs.ofstruct_str","winbase/OFSTRUCT","winbase/POFSTRUCT"]
old-location: fs\ofstruct_str.htm
tech.root: fs
ms.assetid: 195581e5-e962-4756-a33c-b1e898b5b0e7
ms.date: 12/05/2018
ms.keywords: '*LPOFSTRUCT, *POFSTRUCT, OFSTRUCT, OFSTRUCT structure [Files], POFSTRUCT, POFSTRUCT structure pointer [Files], _OFSTRUCT, _win32_ofstruct_str, base.ofstruct_str, fs.ofstruct_str, winbase/OFSTRUCT, winbase/POFSTRUCT'
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFSTRUCT, *LPOFSTRUCT, *POFSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OFSTRUCT
 - winbase/_OFSTRUCT
 - LPOFSTRUCT
 - winbase/LPOFSTRUCT
 - OFSTRUCT
 - winbase/OFSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - OFSTRUCT
---

# OFSTRUCT structure


## -description

Contains information about a file that the 
<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> function opened or attempted to open.

## -struct-fields

### -field cBytes

The size of the structure, in bytes.

### -field fFixedDisk

If this member is nonzero, the file is on a hard (fixed) disk. Otherwise, it is not.

### -field nErrCode

The MS-DOS error code if the 
<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> function failed.

### -field Reserved1

Reserved; do not use.

### -field Reserved2

Reserved; do not use.

### -field szPathName

The path and file name of the file.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>