---
UID: NS:shlobj_core.FILE_ATTRIBUTES_ARRAY
title: FILE_ATTRIBUTES_ARRAY
author: windows-sdk-content
description: Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY.
old-location: shell\FILE_ATTRIBUTES_ARRAY.htm
old-project: shell
ms.assetid: 222a1e97-df2f-49ad-be07-3172f49ecd06
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FILE_ATTRIBUTES_ARRAY, FILE_ATTRIBUTES_ARRAY structure [Windows Shell], _shell_FILE_ATTRIBUTES_ARRAY, shell.FILE_ATTRIBUTES_ARRAY, shlobj_core/FILE_ATTRIBUTES_ARRAY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILE_ATTRIBUTES_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - FILE_ATTRIBUTES_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# FILE_ATTRIBUTES_ARRAY structure


## -description


Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY.


## -struct-fields




### -field cItems

Type: <b>UINT</b>

The number of items in the <b>rgdwFileAttributes</b> array.


### -field dwSumFileAttributes

Type: <b>DWORD</b>

All of the attributes combined using OR.


### -field dwProductFileAttributes

Type: <b>DWORD</b>

All of the attributes combined using AND.


### -field rgdwFileAttributes

Type: <b>DWORD[1]</b>

An array of file attributes.

