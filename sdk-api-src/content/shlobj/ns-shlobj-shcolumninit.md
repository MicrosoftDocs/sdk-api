---
UID: NS:shlobj.SHCOLUMNINIT
title: SHCOLUMNINIT
author: windows-sdk-content
description: Passes initialization information to IColumnProvider::Initialize.
old-location: shell\SHCOLUMNINIT_str.htm
tech.root: shell
ms.assetid: eebe47c8-b3ee-4316-b578-5404ed8f7920
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*LPSHCOLUMNINIT, LPSHCOLUMNINFO, LPSHCOLUMNINFO structure pointer [Windows Shell], SHCOLUMNINIT, SHCOLUMNINIT structure [Windows Shell], _win32_SHCOLUMNINIT_str, shell.SHCOLUMNINIT_str, shlobj/LPSHCOLUMNINFO, shlobj/SHCOLUMNINIT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
 - Shlobj.h
api_name:
 - SHCOLUMNINIT
product: Windows
targetos: Windows
req.typenames: SHCOLUMNINIT, *LPSHCOLUMNINIT
req.redist: 
---

# SHCOLUMNINIT structure


## -description


Passes initialization information to <a href="https://msdn.microsoft.com/4975042d-549e-4032-9f42-468dc7e3c20e">IColumnProvider::Initialize</a>.


## -struct-fields




### -field dwFlags

Type: <b>ULONG</b>

Initialization flags. Reserved. Set to <b>NULL</b>


### -field dwReserved

Type: <b>ULONG</b>

Reserved. Set to <b>NULL</b>.


### -field wszFolder

Type: <b>WCHAR[MAX_PATH]</b>

A pointer to a null-terminated Unicode string with a fully qualified folder path. The string will be empty if multiple folders are specified.

