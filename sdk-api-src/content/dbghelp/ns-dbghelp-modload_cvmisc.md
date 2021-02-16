---
UID: NS:dbghelp._MODLOAD_CVMISC
title: MODLOAD_CVMISC (dbghelp.h)
description: Contains CodeView and Misc records.
helpviewer_keywords: ["*PMODLOAD_CVMISC","MODLOAD_CVMISC","MODLOAD_CVMISC structure","PMODLOAD_CVMISC","PMODLOAD_CVMISC structure pointer","_MODLOAD_CVMISC","base.modload_cvmisc","dbghelp/MODLOAD_CVMISC","dbghelp/PMODLOAD_CVMISC"]
old-location: base\modload_cvmisc.htm
tech.root: Debug
ms.assetid: 24f1ed20-ef7a-4c7b-9bbe-4aaf26c219e7
ms.date: 12/05/2018
ms.keywords: '*PMODLOAD_CVMISC, MODLOAD_CVMISC, MODLOAD_CVMISC structure, PMODLOAD_CVMISC, PMODLOAD_CVMISC structure pointer, _MODLOAD_CVMISC, base.modload_cvmisc, dbghelp/MODLOAD_CVMISC, dbghelp/PMODLOAD_CVMISC'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MODLOAD_CVMISC, *PMODLOAD_CVMISC
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - _MODLOAD_CVMISC
 - dbghelp/_MODLOAD_CVMISC
 - PMODLOAD_CVMISC
 - dbghelp/PMODLOAD_CVMISC
 - MODLOAD_CVMISC
 - dbghelp/MODLOAD_CVMISC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - MODLOAD_CVMISC
---

# MODLOAD_CVMISC structure


## -description

Contains CodeView and Misc records.

## -struct-fields

### -field oCV

The offset of the CodeView record.

### -field cCV

The size of the CodeView record.

### -field oMisc

The offset of the Misc record.

### -field cMisc

The size of the Misc record.

### -field dtImage

The date/time stamp of the image.

### -field cImage

The size of the image.

## -see-also

<a href="/windows/desktop/api/dbghelp/ns-dbghelp-modload_data">MODLOAD_DATA</a>