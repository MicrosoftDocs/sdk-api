---
UID: NE:shlwapi.__unnamed_enum_7
title: ASSOCKEY
author: windows-sdk-content
description: Specifies the type of key to be returned by IQueryAssociations::GetKey.
old-location: shell\ASSOCKEY_str.htm
tech.root: shell
ms.assetid: f4ac0ba0-4113-498f-a51b-74a37fe33d49
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ASSOCKEY, ASSOCKEY enumeration [Windows Shell], ASSOCKEY_APP, ASSOCKEY_BASECLASS, ASSOCKEY_CLASS, ASSOCKEY_SHELLEXECCLASS, _win32_ASSOCKEY_str, shell.ASSOCKEY_str, shlwapi/ASSOCKEY, shlwapi/ASSOCKEY_APP, shlwapi/ASSOCKEY_BASECLASS, shlwapi/ASSOCKEY_CLASS, shlwapi/ASSOCKEY_SHELLEXECCLASS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - ASSOCKEY
product: Windows
targetos: Windows
req.typenames: ASSOCKEY
req.redist: 
---

# ASSOCKEY enumeration


## -description


Specifies the type of key to be returned by <a href="https://msdn.microsoft.com/7f380a9e-fda0-46be-88a1-fd73b0a4b7b7">IQueryAssociations::GetKey</a>.


## -enum-fields




### -field ASSOCKEY_SHELLEXECCLASS

A key that is passed to <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> through a <a href="https://msdn.microsoft.com/50e0dac3-b5dc-4d9f-8fd7-3a53a428166b">SHELLEXECUTEINFO</a> structure.


### -field ASSOCKEY_APP

An <b>Application</b> key for the file type.


### -field ASSOCKEY_CLASS

A ProgID or class key.


### -field ASSOCKEY_BASECLASS

A BaseClass value.


### -field ASSOCKEY_MAX



