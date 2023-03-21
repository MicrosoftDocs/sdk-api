---
UID: NE:shlwapi.tagSFBS_FLAGS
title: tagSFBS_FLAGS (shlwapi.h)
description: Specifies how the StrFormatByteSizeEx function should handle rounding of undisplayed digits.
helpviewer_keywords: ["SFBS_FLAGS","SFBS_FLAGS enumeration [Windows Shell]","SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT","SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS","_shell_SFBS_FLAGS","shell.SFBS_FLAGS","shlwapi/SFBS_FLAGS","shlwapi/SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT","shlwapi/SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS","tagSFBS_FLAGS"]
old-location: shell\SFBS_FLAGS.htm
tech.root: shell
ms.assetid: 9b26734b-bda4-4b60-92a3-fe5b3d360dd0
ms.date: 12/05/2018
ms.keywords: SFBS_FLAGS, SFBS_FLAGS enumeration [Windows Shell], SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT, SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS, _shell_SFBS_FLAGS, shell.SFBS_FLAGS, shlwapi/SFBS_FLAGS, shlwapi/SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT, shlwapi/SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS, tagSFBS_FLAGS
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSFBS_FLAGS
 - shlwapi/tagSFBS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SFBS_FLAGS
---

# tagSFBS_FLAGS enumeration


## -description

Specifies how the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizeex">StrFormatByteSizeEx</a> function should handle rounding of undisplayed digits.

## -enum-fields

### -field SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT:0x0001

Round to the nearest displayed digit.

### -field SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS:0x0002

Discard undisplayed digits.
