---
UID: NS:shlobj_core._SFVM_HELPTOPIC_DATA
title: "_SFVM_HELPTOPIC_DATA"
author: windows-sdk-content
description: Contains the name of an HTML Help file and a topic in that file. Used with the SFVM_GETHELPTOPIC notification. This structure requires Unicode strings.
old-location: shell\SFVM_HELPTOPIC_DATA_str.htm
tech.root: shell
ms.assetid: c06f43ca-be32-4ab7-ba6c-a0066b749dba
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: SFVM_HELPTOPIC_DATA, SFVM_HELPTOPIC_DATA structure [Windows Shell], _SFVM_HELPTOPIC_DATA, _win32_SFVM_HELPTOPIC_DATA_str, shell.SFVM_HELPTOPIC_DATA_str, shlobj_core/SFVM_HELPTOPIC_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SFVM_HELPTOPIC_DATA
product: Windows
targetos: Windows
req.typenames: SFVM_HELPTOPIC_DATA
req.redist: 
---

# _SFVM_HELPTOPIC_DATA structure


## -description


Contains the name of an HTML Help file and a topic in that file. Used with the <a href="https://msdn.microsoft.com/bbe92e9f-4074-4101-a945-072866ab20a8">SFVM_GETHELPTOPIC</a> notification. This structure requires Unicode strings.


## -struct-fields




### -field wszHelpFile

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the fully qualified path to the help file.


### -field wszHelpTopic

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing the name of the topic.

