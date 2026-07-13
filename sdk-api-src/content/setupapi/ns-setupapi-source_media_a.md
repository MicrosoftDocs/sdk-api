---
UID: NS:setupapi._SOURCE_MEDIA_A
title: SOURCE_MEDIA_A (setupapi.h)
description: The SOURCE_MEDIA structure is used with the SPFILENOTIFY_NEEDMEDIA notification to pass source media information. (ANSI)
helpviewer_keywords: ["*PSOURCE_MEDIA_A","PSOURCE_MEDIA","PSOURCE_MEDIA structure pointer [Setup API]","SOURCE_MEDIA","SOURCE_MEDIA structure [Setup API]","SOURCE_MEDIA_A","_setupapi_source_media_str","setup.source_media_str","setupapi/PSOURCE_MEDIA","setupapi/SOURCE_MEDIA"]
old-location: setup\source_media_str.htm
tech.root: setup
ms.assetid: 93a72ec8-b979-4e61-bb06-eed1a6432f16
ms.date: 12/05/2018
ms.keywords: '*PSOURCE_MEDIA_A, PSOURCE_MEDIA, PSOURCE_MEDIA structure pointer [Setup API], SOURCE_MEDIA, SOURCE_MEDIA structure [Setup API], SOURCE_MEDIA_A, _setupapi_source_media_str, setup.source_media_str, setupapi/PSOURCE_MEDIA, setupapi/SOURCE_MEDIA'
req.header: setupapi.h
req.include-header: 
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
req.typenames: SOURCE_MEDIA_A, *PSOURCE_MEDIA_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOURCE_MEDIA_A
 - setupapi/_SOURCE_MEDIA_A
 - PSOURCE_MEDIA_A
 - setupapi/PSOURCE_MEDIA_A
 - SOURCE_MEDIA_A
 - setupapi/SOURCE_MEDIA_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SOURCE_MEDIA
 - source_media_a
---

# SOURCE_MEDIA_A structure


## -description

The 
<b>SOURCE_MEDIA</b> structure is used with the 
<a href="/windows/desktop/SetupApi/spfilenotify-needmedia">SPFILENOTIFY_NEEDMEDIA</a> notification to pass source media information.

## -struct-fields

### -field Reserved

This member is not currently used.

### -field Tagfile

Optional  tag file that can be used to identify the source media.

### -field Description

Human-readable description of the source media.

### -field SourcePath

Path to the source that needs the new media.

### -field SourceFile

Source file to be retrieved from the new media.

### -field Flags

Copy style information that modifies how errors are handled. This member can be one or more of the following values. 







#### SP_COPY_WARNIFSKIP

Inform the user that skipping the file may affect the installation.



#### SP_COPY_NOSKIP

Do not offer the user the option to skip the file.



#### SP_FLAG_CABINETCONTINUATION

The current source file is continued in another cabinet file.



#### SP_COPY_NOBROWSE

Do not offer the user the option to browse.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/spfilenotify-needmedia">SPFILENOTIFY_NEEDMEDIA</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SOURCE_MEDIA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
