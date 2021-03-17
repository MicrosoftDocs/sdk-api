---
UID: NS:usp10.textrange_properties
title: TEXTRANGE_PROPERTIES (usp10.h)
description: Contains a group of OpenType features to apply to a run.
helpviewer_keywords: ["TEXTRANGE_PROPERTIES","TEXTRANGE_PROPERTIES structure [Internationalization for Windows Applications]","_win32_TEXTRANGE_PROPERTIES","intl.textrange_properties","usp10/TEXTRANGE_PROPERTIES"]
old-location: intl\textrange_properties.htm
tech.root: Intl
ms.assetid: f43a0873-f499-4d66-9fce-57f332c1dc77
ms.date: 12/05/2018
ms.keywords: TEXTRANGE_PROPERTIES, TEXTRANGE_PROPERTIES structure [Internationalization for Windows Applications], _win32_TEXTRANGE_PROPERTIES, intl.textrange_properties, usp10/TEXTRANGE_PROPERTIES
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TEXTRANGE_PROPERTIES
req.redist: Usp10.dll version 1.600 or greater onWindows XP
ms.custom: 19H1
f1_keywords:
 - textrange_properties
 - usp10/textrange_properties
 - TEXTRANGE_PROPERTIES
 - usp10/TEXTRANGE_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - TEXTRANGE_PROPERTIES
---

# TEXTRANGE_PROPERTIES structure


## -description

Contains a group of OpenType features to apply to a run.

## -struct-fields

### -field potfRecords

Pointer to an array of <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> structures containing OpenType features (records) to apply to the characters in a specific range of text in a run.

### -field cotfRecords

 Number of features in the array specified by <b>potfRecords</b>.

## -see-also

<a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>