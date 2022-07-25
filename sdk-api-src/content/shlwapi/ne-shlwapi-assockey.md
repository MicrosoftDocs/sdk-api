---
UID: NE:shlwapi.__unnamed_enum_7
title: ASSOCKEY (shlwapi.h)
description: Specifies the type of key to be returned by IQueryAssociations::GetKey.
helpviewer_keywords: ["ASSOCKEY","ASSOCKEY enumeration [Windows Shell]","ASSOCKEY_APP","ASSOCKEY_BASECLASS","ASSOCKEY_CLASS","ASSOCKEY_SHELLEXECCLASS","_win32_ASSOCKEY_str","shell.ASSOCKEY_str","shlwapi/ASSOCKEY","shlwapi/ASSOCKEY_APP","shlwapi/ASSOCKEY_BASECLASS","shlwapi/ASSOCKEY_CLASS","shlwapi/ASSOCKEY_SHELLEXECCLASS"]
old-location: shell\ASSOCKEY_str.htm
tech.root: shell
ms.assetid: f4ac0ba0-4113-498f-a51b-74a37fe33d49
ms.date: 12/05/2018
ms.keywords: ASSOCKEY, ASSOCKEY enumeration [Windows Shell], ASSOCKEY_APP, ASSOCKEY_BASECLASS, ASSOCKEY_CLASS, ASSOCKEY_SHELLEXECCLASS, _win32_ASSOCKEY_str, shell.ASSOCKEY_str, shlwapi/ASSOCKEY, shlwapi/ASSOCKEY_APP, shlwapi/ASSOCKEY_BASECLASS, shlwapi/ASSOCKEY_CLASS, shlwapi/ASSOCKEY_SHELLEXECCLASS
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ASSOCKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASSOCKEY
 - shlwapi/ASSOCKEY
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
 - ASSOCKEY
---

# ASSOCKEY enumeration


## -description

Specifies the type of key to be returned by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey">IQueryAssociations::GetKey</a>.

## -enum-fields

### -field ASSOCKEY_SHELLEXECCLASS:1

A key that is passed to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> through a <a href="/windows/desktop/api/shellapi/ns-shellapi-shellexecuteinfoa">SHELLEXECUTEINFO</a> structure.

### -field ASSOCKEY_APP

An <b>Application</b> key for the file type.

### -field ASSOCKEY_CLASS

A ProgID or class key.

### -field ASSOCKEY_BASECLASS

A BaseClass value.

### -field ASSOCKEY_MAX
