---
UID: NS:shlobj_core._SFVM_HELPTOPIC_DATA
title: SFVM_HELPTOPIC_DATA (shlobj_core.h)
description: Contains the name of an HTML Help file and a topic in that file. Used with the SFVM_GETHELPTOPIC notification. This structure requires Unicode strings.
helpviewer_keywords: ["SFVM_HELPTOPIC_DATA","SFVM_HELPTOPIC_DATA structure [Windows Shell]","_SFVM_HELPTOPIC_DATA","_win32_SFVM_HELPTOPIC_DATA_str","shell.SFVM_HELPTOPIC_DATA_str","shlobj_core/SFVM_HELPTOPIC_DATA"]
old-location: shell\SFVM_HELPTOPIC_DATA_str.htm
tech.root: shell
ms.assetid: c06f43ca-be32-4ab7-ba6c-a0066b749dba
ms.date: 12/05/2018
ms.keywords: SFVM_HELPTOPIC_DATA, SFVM_HELPTOPIC_DATA structure [Windows Shell], _SFVM_HELPTOPIC_DATA, _win32_SFVM_HELPTOPIC_DATA_str, shell.SFVM_HELPTOPIC_DATA_str, shlobj_core/SFVM_HELPTOPIC_DATA
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: SFVM_HELPTOPIC_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SFVM_HELPTOPIC_DATA
 - shlobj_core/_SFVM_HELPTOPIC_DATA
 - SFVM_HELPTOPIC_DATA
 - shlobj_core/SFVM_HELPTOPIC_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SFVM_HELPTOPIC_DATA
---

# SFVM_HELPTOPIC_DATA structure


## -description

Contains the name of an HTML Help file and a topic in that file. Used with the <a href="/windows/desktop/shell/sfvm-gethelptopic">SFVM_GETHELPTOPIC</a> notification. This structure requires Unicode strings.

## -struct-fields

### -field wszHelpFile

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the fully qualified path to the help file.

### -field wszHelpTopic

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the name of the topic.