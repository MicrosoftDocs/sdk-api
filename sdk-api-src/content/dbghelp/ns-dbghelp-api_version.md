---
UID: NS:dbghelp.API_VERSION
title: API_VERSION (dbghelp.h)
description: Contains the library version.
helpviewer_keywords: ["*LPAPI_VERSION","API_VERSION","API_VERSION structure","LPAPI_VERSION","LPAPI_VERSION structure pointer","_win32_api_version_str","base.api_version_str","dbghelp/API_VERSION","dbghelp/LPAPI_VERSION"]
old-location: base\api_version_str.htm
tech.root: Debug
ms.assetid: f983f639-6a94-4b83-a443-0d98b85d3950
ms.date: 12/05/2018
ms.keywords: '*LPAPI_VERSION, API_VERSION, API_VERSION structure, LPAPI_VERSION, LPAPI_VERSION structure pointer, _win32_api_version_str, base.api_version_str, dbghelp/API_VERSION, dbghelp/LPAPI_VERSION'
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
req.typenames: API_VERSION, *LPAPI_VERSION
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - API_VERSION
 - dbghelp/API_VERSION
 - LPAPI_VERSION
 - dbghelp/LPAPI_VERSION
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
 - API_VERSION
---

# API_VERSION structure


## -description

Contains the library version.

## -struct-fields

### -field MajorVersion

The major version number.

### -field MinorVersion

The minor version number.

### -field Revision

The revision number.

### -field Reserved

This member is reserved for use by the operating system.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagehlpapiversion">ImagehlpApiVersion</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagehlpapiversionex">ImagehlpApiVersionEx</a>