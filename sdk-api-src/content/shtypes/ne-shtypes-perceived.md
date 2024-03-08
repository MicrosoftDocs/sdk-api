---
UID: NE:shtypes.tagPERCEIVED
title: PERCEIVED (shtypes.h)
description: Specifies a file's perceived type. This set of constants is used in the AssocGetPerceivedType function.
helpviewer_keywords: ["PERCEIVED","PERCEIVED enumeration [Windows Shell]","PERCEIVED_TYPE_APPLICATION","PERCEIVED_TYPE_AUDIO","PERCEIVED_TYPE_COMPRESSED","PERCEIVED_TYPE_CONTACTS","PERCEIVED_TYPE_CUSTOM","PERCEIVED_TYPE_DOCUMENT","PERCEIVED_TYPE_FOLDER","PERCEIVED_TYPE_GAMEMEDIA","PERCEIVED_TYPE_IMAGE","PERCEIVED_TYPE_SYSTEM","PERCEIVED_TYPE_TEXT","PERCEIVED_TYPE_UNKNOWN","PERCEIVED_TYPE_UNSPECIFIED","PERCEIVED_TYPE_VIDEO","_shell_PERCEIVED","shell.PERCEIVED","shtypes/PERCEIVED","shtypes/PERCEIVED_TYPE_APPLICATION","shtypes/PERCEIVED_TYPE_AUDIO","shtypes/PERCEIVED_TYPE_COMPRESSED","shtypes/PERCEIVED_TYPE_CONTACTS","shtypes/PERCEIVED_TYPE_CUSTOM","shtypes/PERCEIVED_TYPE_DOCUMENT","shtypes/PERCEIVED_TYPE_FOLDER","shtypes/PERCEIVED_TYPE_GAMEMEDIA","shtypes/PERCEIVED_TYPE_IMAGE","shtypes/PERCEIVED_TYPE_SYSTEM","shtypes/PERCEIVED_TYPE_TEXT","shtypes/PERCEIVED_TYPE_UNKNOWN","shtypes/PERCEIVED_TYPE_UNSPECIFIED","shtypes/PERCEIVED_TYPE_VIDEO"]
old-location: shell\PERCEIVED.htm
tech.root: shell
ms.assetid: dbaf5894-1ed6-446f-ac15-12ba4c7326e7
ms.date: 12/05/2018
ms.keywords: PERCEIVED, PERCEIVED enumeration [Windows Shell], PERCEIVED_TYPE_APPLICATION, PERCEIVED_TYPE_AUDIO, PERCEIVED_TYPE_COMPRESSED, PERCEIVED_TYPE_CONTACTS, PERCEIVED_TYPE_CUSTOM, PERCEIVED_TYPE_DOCUMENT, PERCEIVED_TYPE_FOLDER, PERCEIVED_TYPE_GAMEMEDIA, PERCEIVED_TYPE_IMAGE, PERCEIVED_TYPE_SYSTEM, PERCEIVED_TYPE_TEXT, PERCEIVED_TYPE_UNKNOWN, PERCEIVED_TYPE_UNSPECIFIED, PERCEIVED_TYPE_VIDEO, _shell_PERCEIVED, shell.PERCEIVED, shtypes/PERCEIVED, shtypes/PERCEIVED_TYPE_APPLICATION, shtypes/PERCEIVED_TYPE_AUDIO, shtypes/PERCEIVED_TYPE_COMPRESSED, shtypes/PERCEIVED_TYPE_CONTACTS, shtypes/PERCEIVED_TYPE_CUSTOM, shtypes/PERCEIVED_TYPE_DOCUMENT, shtypes/PERCEIVED_TYPE_FOLDER, shtypes/PERCEIVED_TYPE_GAMEMEDIA, shtypes/PERCEIVED_TYPE_IMAGE, shtypes/PERCEIVED_TYPE_SYSTEM, shtypes/PERCEIVED_TYPE_TEXT, shtypes/PERCEIVED_TYPE_UNKNOWN, shtypes/PERCEIVED_TYPE_UNSPECIFIED, shtypes/PERCEIVED_TYPE_VIDEO
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PERCEIVED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPERCEIVED
 - shtypes/tagPERCEIVED
 - PERCEIVED
 - shtypes/PERCEIVED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - PERCEIVED
---

# PERCEIVED enumeration


## -description

Specifies a file's perceived type. This set of constants is used in the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocgetperceivedtype">AssocGetPerceivedType</a> function.

## -enum-fields

### -field PERCEIVED_TYPE_FIRST:-3

### -field PERCEIVED_TYPE_CUSTOM:-3

The file's perceived type as defined in the registry is not a known type.

### -field PERCEIVED_TYPE_UNSPECIFIED:-2

The file does not have a perceived type.

### -field PERCEIVED_TYPE_FOLDER:-1

Not used.

### -field PERCEIVED_TYPE_UNKNOWN:0

The file's perceived type hasn't yet been requested. This is the cached type of the object when it is created. This value is never returned by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocgetperceivedtype">AssocGetPerceivedType</a>.

### -field PERCEIVED_TYPE_TEXT:1

The file's perceived type is "text".

### -field PERCEIVED_TYPE_IMAGE:2

The file's perceived type is "image".

### -field PERCEIVED_TYPE_AUDIO:3

The file's perceived type is "audio".

### -field PERCEIVED_TYPE_VIDEO:4

The file's perceived type is "video".

### -field PERCEIVED_TYPE_COMPRESSED:5

The file's perceived type is "compressed".

### -field PERCEIVED_TYPE_DOCUMENT:6

The file's perceived type is "document".

### -field PERCEIVED_TYPE_SYSTEM:7

The file's perceived type is "system".

### -field PERCEIVED_TYPE_APPLICATION:8

The file's perceived type is "application".

### -field PERCEIVED_TYPE_GAMEMEDIA:9

<b>Windows Vista and later</b>. The file's perceived type is "gamemedia".

### -field PERCEIVED_TYPE_CONTACTS:10

<b>Windows Vista and later</b>.The file's perceived type is "contacts"

### -field PERCEIVED_TYPE_LAST:10

## -remarks

Prior to Windows Vista, this enumeration was declared in Shlwapi.h.
