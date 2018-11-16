---
UID: NF:shlobj_core.SHGetSetSettings
title: SHGetSetSettings function
author: windows-sdk-content
description: SHGetSetSettings may be altered or unavailable.
old-location: shell\SHGetSetSettings.htm
tech.root: shell
ms.assetid: d7c2646c-03e0-4d7a-9503-bdf487d43723
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SHGetSetSettings, SHGetSetSettings function [Windows Shell], _win32_SHGetSetSettings, shell.SHGetSetSettings, shlobj_core/SHGetSetSettings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetSetSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHGetSetSettings
: 
---

# SHGetSetSettings function


## -description


<p class="CCE_Message">[<b>SHGetSetSettings</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets or retrieves Shell state settings.


## -parameters




### -param lpss [in, out]

Type: <b>LPSHELLSTATE</b>

A pointer to a <a href="https://msdn.microsoft.com/a5ba0e9f-d164-4fe6-97ab-34d61289ce1c">SHELLSTATE</a> structure that provides or receives the Shell state settings.


### -param dwMask [in]

Type: <b>DWORD</b>

One or more of the <a href="https://msdn.microsoft.com/2a883110-fdc3-4451-9e47-e58894600e3b">SSF</a> flags that indicate which settings should be set or retrieved.


### -param bSet [in]

Type: <b>BOOL</b>

<b>TRUE</b> to indicate that the contents of <i>lpss</i> should be used to set the Shell settings, <b>FALSE</b> to indicate that the Shell settings should be retrieved to <i>lpss</i>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/728a4004-f35d-4592-baf1-456a613a3344">SHGetSettings</a>
 

 

