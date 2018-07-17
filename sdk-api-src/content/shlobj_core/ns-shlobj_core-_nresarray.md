---
UID: NS:shlobj_core._NRESARRAY
title: "_NRESARRAY"
author: windows-sdk-content
description: Defines the CF_NETRESOURCE clipboard format.
old-location: shell\NRESARRAY.htm
old-project: shell
ms.assetid: 261338c2-8fb4-4d10-8392-f9f6254a30ed
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*LPNRESARRAY, LPNRESARRAY, LPNRESARRAY structure pointer [Windows Shell], NRESARRAY, NRESARRAY structure [Windows Shell], _NRESARRAY, _win32_NRESARRAY, shell.NRESARRAY, shlobj_core/LPNRESARRAY, shlobj_core/NRESARRAY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: NRESARRAY, *LPNRESARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - NRESARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _NRESARRAY structure


## -description


Defines the CF_NETRESOURCE clipboard format.


## -struct-fields




### -field cItems

Type: <b>UINT</b>

The number of elements in the <b>nr</b> array.


### -field nr

Type: <b><a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>[1]</b>

The array of <a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structures that contain information about network resources. The string members (<b>LPSTR</b> types) in the structure contain offsets instead of addresses.

