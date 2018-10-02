---
UID: NE:shlwapi.tagSFBS_FLAGS
title: tagSFBS_FLAGS
author: windows-sdk-content
description: Specifies how the StrFormatByteSizeEx function should handle rounding of undisplayed digits.
old-location: shell\SFBS_FLAGS.htm
tech.root: Shell
ms.assetid: 9b26734b-bda4-4b60-92a3-fe5b3d360dd0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SFBS_FLAGS, SFBS_FLAGS enumeration [Windows Shell], SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT, SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS, _shell_SFBS_FLAGS, shell.SFBS_FLAGS, shlwapi/SFBS_FLAGS, shlwapi/SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT, shlwapi/SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS, tagSFBS_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SFBS_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# tagSFBS_FLAGS enumeration


## -description


Specifies how the <a href="https://msdn.microsoft.com/9ecc6427-e7bb-43ec-ab78-665ef52f8b10">StrFormatByteSizeEx</a> function should handle rounding of undisplayed digits.


## -enum-fields




### -field SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT

Round to the nearest displayed digit.


### -field SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS

Discard undisplayed digits.

