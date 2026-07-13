---
UID: NC:psapi.PENUM_PAGE_FILE_CALLBACKA
title: PENUM_PAGE_FILE_CALLBACKA (psapi.h)
description: An application-defined callback function used with the EnumPageFiles function. (ANSI)
helpviewer_keywords: ["EnumPageFilesProc","EnumPageFilesProc callback","EnumPageFilesProc callback function [PSAPI]","PENUM_PAGE_FILE_CALLBACKA","PENUM_PAGE_FILE_CALLBACKW","_win32_enumpagefilesproc","base.enumpagefilesproc","psapi.enumpagefilesproc","psapi/EnumPageFilesProc","psapi/PENUM_PAGE_FILE_CALLBACKA","psapi/PENUM_PAGE_FILE_CALLBACKW"]
old-location: psapi\enumpagefilesproc.htm
tech.root: psapi
ms.assetid: eb3610fb-2c95-4f7b-973d-8dc41d2829f1
ms.date: 12/05/2018
ms.keywords: EnumPageFilesProc, EnumPageFilesProc callback, EnumPageFilesProc callback function [PSAPI], PENUM_PAGE_FILE_CALLBACKA, PENUM_PAGE_FILE_CALLBACKW, _win32_enumpagefilesproc, base.enumpagefilesproc, psapi.enumpagefilesproc, psapi/EnumPageFilesProc, psapi/PENUM_PAGE_FILE_CALLBACKA, psapi/PENUM_PAGE_FILE_CALLBACKW
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PENUM_PAGE_FILE_CALLBACKW (Unicode) and PENUM_PAGE_FILE_CALLBACKA (ANSI)
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
 - PENUM_PAGE_FILE_CALLBACKA
 - psapi/PENUM_PAGE_FILE_CALLBACKA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Psapi.h
api_name:
 - EnumPageFilesProc
 - PENUM_PAGE_FILE_CALLBACKA
 - PENUM_PAGE_FILE_CALLBACKW
---

# PENUM_PAGE_FILE_CALLBACKA callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/psapi/nf-psapi-enumpagefilesa">EnumPageFiles</a> function.

The <b>PENUM_PAGE_FILE_CALLBACK</b> type defines a pointer to this callback function. 
<b>EnumPageFilesProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param pContext [in]

The user-defined data passed from 
<a href="/windows/desktop/api/psapi/nf-psapi-enumpagefilesa">EnumPageFiles</a>.

### -param pPageFileInfo [in]

A pointer to an 
<a href="/windows/desktop/api/psapi/ns-psapi-enum_page_file_information">ENUM_PAGE_FILE_INFORMATION</a> structure.

### -param lpFilename [in]

The name of the pagefile.

## -returns

To continue enumeration, the callback function must return TRUE.

To stop enumeration, the callback function must return FALSE.

## -see-also

<a href="/windows/desktop/api/psapi/ns-psapi-enum_page_file_information">ENUM_PAGE_FILE_INFORMATION</a>



<a href="/windows/desktop/api/psapi/nf-psapi-enumpagefilesa">EnumPageFiles</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>

## -remarks

> [!NOTE]
> The psapi.h header defines PENUM_PAGE_FILE_CALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
