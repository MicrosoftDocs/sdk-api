---
UID: NS:usp10.opentype_feature_record
title: OPENTYPE_FEATURE_RECORD (usp10.h)
description: Contains information about a single OpenType feature to apply to a run.
helpviewer_keywords: ["OPENTYPE_FEATURE_RECORD","OPENTYPE_FEATURE_RECORD structure [Internationalization for Windows Applications]","_win32_OPENTYPE_FEATURE_RECORD","intl.opentype_feature_record","usp10/OPENTYPE_FEATURE_RECORD"]
old-location: intl\opentype_feature_record.htm
tech.root: Intl
ms.assetid: 3f4d76f7-fd50-4a38-973b-329e477e5960
ms.date: 12/05/2018
ms.keywords: OPENTYPE_FEATURE_RECORD, OPENTYPE_FEATURE_RECORD structure [Internationalization for Windows Applications], _win32_OPENTYPE_FEATURE_RECORD, intl.opentype_feature_record, usp10/OPENTYPE_FEATURE_RECORD
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
req.typenames: OPENTYPE_FEATURE_RECORD
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
f1_keywords:
 - opentype_feature_record
 - usp10/opentype_feature_record
 - OPENTYPE_FEATURE_RECORD
 - usp10/OPENTYPE_FEATURE_RECORD
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
 - OPENTYPE_FEATURE_RECORD
---

# OPENTYPE_FEATURE_RECORD structure


## -description

Contains information about a single OpenType feature to apply to a run.

## -struct-fields

### -field tagFeature

<a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure containing a registered or private OpenType feature tag. For information on feature tags, see <a href="/typography/opentype/spec/featuretags">http://www.microsoft.com/typography/otspec/featuretags.htm</a>.

### -field lParameter

Value indicating how to apply the feature tag. Possible values are defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Feature is disabled and should not be applied.</td>
</tr>
<tr>
<td>1</td>
<td>Feature is active. If the feature offers several alternatives, select the first value.</td>
</tr>
<tr>
<td>Greater than 1</td>
<td>Feature is active. Select the alternative value at this index. Should be used only when multiple alternatives are available for a feature.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a>



<a href="/windows/desktop/api/usp10/ns-usp10-textrange_properties">TEXTRANGE_PROPERTIES</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>
