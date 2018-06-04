---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagQUERY_PARSER_MANAGER_OPTION enumeration


## -description


Used by <a href="https://msdn.microsoft.com/54cb5501-bb53-4be5-8b0b-a2ea754c778a">IQueryParserManager::SetOption</a> to set parsing options. This can be used to specify schemas and localization options.


## -enum-fields




### -field QPMO_SCHEMA_BINARY_NAME

A <b>VT_LPWSTR</b> containing the name of the file that contains the schema binary. The default value is <b>StructuredQuerySchema.bin</b> for the SystemIndex catalog and <b>StructuredQuerySchemaTrivial.bin</b> for the trivial catalog.


### -field QPMO_PRELOCALIZED_SCHEMA_BINARY_PATH

Either a <b>VT_BOOL</b> or a <b>VT_LPWSTR</b>. If the value is a <b>VT_BOOL</b> and is <b>FALSE</b>, a pre-localized schema will not be used. If the value is a <b>VT_BOOL</b> and is <b>TRUE</b>, <a href="https://msdn.microsoft.com/ff1941e1-03f0-4fdb-a34b-61da4055f569">IQueryParserManager</a> will use the pre-localized schema binary in "<code>%ALLUSERSPROFILE%\Microsoft\Windows</code>". If the value is a <b>VT_LPWSTR</b>, the value should contain the full path of the folder in which the pre-localized schema binary can be found. The default value is <b>VT_BOOL</b> with <b>TRUE</b>.


### -field QPMO_UNLOCALIZED_SCHEMA_BINARY_PATH

A <b>VT_LPWSTR</b> containing the full path to the folder that contains the unlocalized schema binary. The default value is "<code>%SYSTEMROOT%\System32</code>".


### -field QPMO_LOCALIZED_SCHEMA_BINARY_PATH

A <b>VT_LPWSTR</b> containing the full path to the folder that contains the localized schema binary that can be read and written to as needed. The default value is "<code>%LOCALAPPDATA%\Microsoft\Windows</code>".


### -field QPMO_APPEND_LCID_TO_LOCALIZED_PATH

A <b>VT_BOOL</b>.  If <b>TRUE</b>, then the paths for pre-localized and localized binaries have "<code>\(LCID)</code>" appended to them, where LCID is the decimal locale ID for the localized language. The default is <b>TRUE</b>.


### -field QPMO_LOCALIZER_SUPPORT

A <b>VT_UNKNOWN</b> with an object supporting <a href="https://msdn.microsoft.com/7db4c6ec-ba3a-49dd-bba5-3847d4d74e06">ISchemaLocalizerSupport</a>. This object will be used instead of the default localizer support object.

