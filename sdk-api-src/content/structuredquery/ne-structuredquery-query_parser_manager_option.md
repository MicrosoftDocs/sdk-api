---
UID: NE:structuredquery.tagQUERY_PARSER_MANAGER_OPTION
title: QUERY_PARSER_MANAGER_OPTION (structuredquery.h)
description: Used by IQueryParserManager::SetOption to set parsing options. This can be used to specify schemas and localization options.
helpviewer_keywords: ["QPMO_APPEND_LCID_TO_LOCALIZED_PATH","QPMO_LOCALIZED_SCHEMA_BINARY_PATH","QPMO_LOCALIZER_SUPPORT","QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH","QPMO_SCHEMA_BINARY_NAME","QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH","QUERY_PARSER_MANAGER_OPTION","QUERY_PARSER_MANAGER_OPTION enumeration [search]","_search_QUERY_PARSER_MANAGER_OPTION","search._search_QUERY_PARSER_MANAGER_OPTION","structuredquery/QPMO_APPEND_LCID_TO_LOCALIZED_PATH","structuredquery/QPMO_LOCALIZED_SCHEMA_BINARY_PATH","structuredquery/QPMO_LOCALIZER_SUPPORT","structuredquery/QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH","structuredquery/QPMO_SCHEMA_BINARY_NAME","structuredquery/QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH","structuredquery/QUERY_PARSER_MANAGER_OPTION"]
old-location: search\_search_QUERY_PARSER_MANAGER_OPTION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\query_parser_manager_option.htm
ms.date: 12/05/2018
ms.keywords: QPMO_APPEND_LCID_TO_LOCALIZED_PATH, QPMO_LOCALIZED_SCHEMA_BINARY_PATH, QPMO_LOCALIZER_SUPPORT, QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH, QPMO_SCHEMA_BINARY_NAME, QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH, QUERY_PARSER_MANAGER_OPTION, QUERY_PARSER_MANAGER_OPTION enumeration [search], _search_QUERY_PARSER_MANAGER_OPTION, search._search_QUERY_PARSER_MANAGER_OPTION, structuredquery/QPMO_APPEND_LCID_TO_LOCALIZED_PATH, structuredquery/QPMO_LOCALIZED_SCHEMA_BINARY_PATH, structuredquery/QPMO_LOCALIZER_SUPPORT, structuredquery/QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH, structuredquery/QPMO_SCHEMA_BINARY_NAME, structuredquery/QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH, structuredquery/QUERY_PARSER_MANAGER_OPTION
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QUERY_PARSER_MANAGER_OPTION
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagQUERY_PARSER_MANAGER_OPTION
 - structuredquery/tagQUERY_PARSER_MANAGER_OPTION
 - QUERY_PARSER_MANAGER_OPTION
 - structuredquery/QUERY_PARSER_MANAGER_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquery.h
api_name:
 - QUERY_PARSER_MANAGER_OPTION
---

# QUERY_PARSER_MANAGER_OPTION enumeration


## -description

Used by <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-setoption">IQueryParserManager::SetOption</a> to set parsing options. This can be used to specify schemas and localization options.

## -enum-fields

### -field QPMO_SCHEMA_BINARY_NAME:0

A <b>VT_LPWSTR</b> containing the name of the file that contains the schema binary. The default value is <b>StructuredQuerySchema.bin</b> for the SystemIndex catalog and <b>StructuredQuerySchemaTrivial.bin</b> for the trivial catalog.

### -field QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH

Either a <b>VT_BOOL</b> or a <b>VT_LPWSTR</b>. If the value is a <b>VT_BOOL</b> and is <b>FALSE</b>, a pre-localized schema will not be used. If the value is a <b>VT_BOOL</b> and is <b>TRUE</b>, <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparsermanager">IQueryParserManager</a> will use the pre-localized schema binary in "<code>%ALLUSERSPROFILE%\Microsoft\Windows</code>". If the value is a <b>VT_LPWSTR</b>, the value should contain the full path of the folder in which the pre-localized schema binary can be found. The default value is <b>VT_BOOL</b> with <b>TRUE</b>.

### -field QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH

A <b>VT_LPWSTR</b> containing the full path to the folder that contains the unlocalized schema binary. The default value is "<code>%SYSTEMROOT%\System32</code>".

### -field QPMO_LOCALIZED_SCHEMA_BINARY_PATH

A <b>VT_LPWSTR</b> containing the full path to the folder that contains the localized schema binary that can be read and written to as needed. The default value is "<code>%LOCALAPPDATA%\Microsoft\Windows</code>".

### -field QPMO_APPEND_LCID_TO_LOCALIZED_PATH

A <b>VT_BOOL</b>.  If <b>TRUE</b>, then the paths for pre-localized and localized binaries have "<code>\(LCID)</code>" appended to them, where LCID is the decimal locale ID for the localized language. The default is <b>TRUE</b>.

### -field QPMO_LOCALIZER_SUPPORT

A <b>VT_UNKNOWN</b> with an object supporting <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemalocalizersupport">ISchemaLocalizerSupport</a>. This object will be used instead of the default localizer support object.
