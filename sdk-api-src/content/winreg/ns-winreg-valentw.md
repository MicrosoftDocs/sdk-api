---
UID: NS:winreg.value_entW
title: VALENTW (winreg.h)
description: Contains information about a registry value. The RegQueryMultipleValues function uses this structure. (Unicode)
helpviewer_keywords: ["*PVALENTW","PVALENT","PVALENT structure pointer","VALENT","VALENT structure","VALENTA","VALENTW","_win32_valent_str","base.valent_str","winreg/PVALENT","winreg/VALENT","winreg/VALENTA","winreg/VALENTW"]
old-location: base\valent_str.htm
tech.root: winprog
ms.assetid: 7881eea8-e4e3-48cf-ba8f-b5c23910ae7d
ms.date: 12/05/2018
ms.keywords: '*PVALENTW, PVALENT, PVALENT structure pointer, VALENT, VALENT structure, VALENTA, VALENTW, _win32_valent_str, base.valent_str, winreg/PVALENT, winreg/VALENT, winreg/VALENTA, winreg/VALENTW'
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VALENTW (Unicode) and VALENTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VALENTW, *PVALENTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - value_entW
 - winreg/value_entW
 - PVALENTW
 - winreg/PVALENTW
 - VALENTW
 - winreg/VALENTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winreg.h
api_name:
 - VALENT
 - VALENTA
 - VALENTW
---

# VALENTW structure


## -description

Contains information about a registry value. The 
<a href="/windows/desktop/api/winreg/nf-winreg-regquerymultiplevaluesa">RegQueryMultipleValues</a> function uses this structure.

## -struct-fields

### -field ve_valuename

The name of the value to be retrieved. Be sure to set this member before calling 
<a href="/windows/desktop/api/winreg/nf-winreg-regquerymultiplevaluesa">RegQueryMultipleValues</a>.

### -field ve_valuelen

The size of the data pointed to by <b>ve_valueptr</b>, in bytes.

### -field ve_valueptr

A pointer to the data for the value entry. This is a pointer to the value's data returned in the <b>lpValueBuf</b> buffer filled in by 
<a href="/windows/desktop/api/winreg/nf-winreg-regquerymultiplevaluesa">RegQueryMultipleValues</a>.

### -field ve_type

The type of data pointed to by <b>ve_valueptr</b>. For a list of the possible types, see 
<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regquerymultiplevaluesa">RegQueryMultipleValues</a>

## -remarks

> [!NOTE]
> The winreg.h header defines VALENT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
