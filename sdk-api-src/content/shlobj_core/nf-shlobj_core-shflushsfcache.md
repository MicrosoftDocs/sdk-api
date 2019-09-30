---
UID: NF:shlobj_core.SHFlushSFCache
title: SHFlushSFCache function (shlobj_core.h)
author: windows-sdk-content
description: SHFlushSFCache may be altered or unavailable.
old-location: shell\SHFlushSFCache.htm
tech.root: shell
ms.assetid: 2e39b6b1-e60c-411c-aabc-5a3511f0693b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHFlushSFCache, SHFlushSFCache function [Windows Shell], _win32_SHFlushSFCache, shell.SHFlushSFCache, shlobj_core/SHFlushSFCache
ms.topic: function
f1_keywords: 
 - "shlobj_core/SHFlushSFCache"
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-Ms-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHFlushSFCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHFlushSFCache function


## -description


<p class="CCE_Message">[<b>SHFlushSFCache</b> is available for use in the operating 
    systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Flushes the special folder cache.


## -parameters






## -returns



This function does not return a value.




## -remarks



<b>SHFlushSFCache</b> is called when the path to a special 
    folder is changed. This ensures that the updated path stored in the registry is used rather than the cached 
    value.

For more information on special folders, see the <i>Special Folders and CSIDLs</i> section 
    of <a href="https://docs.microsoft.com/windows/desktop/shell/folder-id">Getting a Folder's ID</a>.



