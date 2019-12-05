---
UID: NS:setupapi._SOURCE_MEDIA_W
title: SOURCE_MEDIA_W (setupapi.h)
description: The SOURCE_MEDIA structure is used with the SPFILENOTIFY_NEEDMEDIA notification to pass source media information.
old-location: setup\source_media_str.htm
tech.root: SetupApi
ms.assetid: 93a72ec8-b979-4e61-bb06-eed1a6432f16
ms.date: 12/05/2018
ms.keywords: '*PSOURCE_MEDIA_W, PSOURCE_MEDIA, PSOURCE_MEDIA structure pointer [Setup API], SOURCE_MEDIA, SOURCE_MEDIA structure [Setup API], SOURCE_MEDIA_W, _setupapi_source_media_str, setup.source_media_str, setupapi/PSOURCE_MEDIA, setupapi/SOURCE_MEDIA'
ms.topic: struct
f1_keywords:
- setupapi/SOURCE_MEDIA
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Setupapi.h
api_name:
- SOURCE_MEDIA
- source_media_w
targetos: Windows
req.typenames: SOURCE_MEDIA_W, *PSOURCE_MEDIA_W
req.redist: 
ms.custom: 19H1
---

# SOURCE_MEDIA_W structure


## -description


The 
<b>SOURCE_MEDIA</b> structure is used with the 
<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-needmedia">SPFILENOTIFY_NEEDMEDIA</a> notification to pass source media information.


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


##### - Flags.SP_COPY_NOBROWSE

Do not offer the user the option to browse.


##### - Flags.SP_COPY_NOSKIP

Do not offer the user the option to skip the file.


##### - Flags.SP_COPY_WARNIFSKIP

Inform the user that skipping the file may affect the installation.


##### - Flags.SP_FLAG_CABINETCONTINUATION

The current source file is continued in another cabinet file.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-needmedia">SPFILENOTIFY_NEEDMEDIA</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/structures--setup-api-">Structures</a>
 

 

