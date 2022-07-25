---
UID: NC:gdiplustypes.EnumerateMetafileProc
title: EnumerateMetafileProc
ms.date: 11/4/2019
targetos: Windows
description: \**EnumerateMetafileProc** is the signature of a callback function that you implement in your application for the [**Graphics::EnumerateMetafile**](../gdiplusgraphics/nf-gdiplusgraphics-graphics-enumeratemetafile(constmetafile_constpointf_int_constrectf__unit_enumeratemetafileproc_void_constimageattributes).md) method (and overloads).
tech.root: gdiplus
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplustypes.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - gdiplustypes.h
api_name:
 - EnumerateMetafileProc
f1_keywords:
 - EnumerateMetafileProc
 - gdiplustypes/EnumerateMetafileProc
dev_langs:
 - c++
---

## -description

**EnumerateMetafileProc** is the signature of a callback function that you implement in your application for the [**Graphics::EnumerateMetafile**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-enumeratemetafile(constmetafile_constpointf_int_constrectf__unit_enumeratemetafileproc_void_constimageattributes)) method (and overloads).

In turn, your implementation can call [**Metafile::PlayRecord**](../gdiplusheaders/nf-gdiplusheaders-metafile-playrecord.md) to play the record that was just enumerated.

## -parameters

### -param unnamedParam1

Type: **[EmfPlusRecordType](../gdiplusenums/ne-gdiplusenums-emfplusrecordtype.md)**

The WMF, EMF, or EMF+ record type.

### -param unnamedParam2

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

Flags; always 0 for WMF/EMF records.

### -param unnamedParam3

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The size of the record data (in bytes), or 0 if no data.

### -param unnamedParam4

Type: **[BYTE](/windows/win32/winprog/windows-data-types)***

A pointer to the record data, or **NULL** if no data.

### -param unnamedParam5

Type: **[VOID](/windows/win32/winprog/windows-data-types)\***

A pointer to callbackData, if any.

## -returns

Return **FALSE** to abort the enumeration process; return **TRUE** to continue it.

## -remarks

## -see-also
