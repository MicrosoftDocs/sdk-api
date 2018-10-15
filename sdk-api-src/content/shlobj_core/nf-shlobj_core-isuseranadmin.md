---
UID: NF:shlobj_core.IsUserAnAdmin
title: IsUserAnAdmin function
author: windows-sdk-content
description: IsUserAnAdmin may be altered or unavailable.
old-location: shell\IsUserAnAdmin.htm
tech.root: shell
ms.assetid: fe698d32-32f6-4b2b-ad0c-5d9ec815177f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IsUserAnAdmin, IsUserAnAdmin function [Windows Shell], _win32_IsUserAnAdmin, shell.IsUserAnAdmin, shlobj_core/IsUserAnAdmin
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - IsUserAnAdmin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsUserAnAdmin function


## -description


<p class="CCE_Message">[<b>IsUserAnAdmin</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Tests whether the current user is a member of the Administrator's group.


## -parameters






## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the user is a member of the Administrator's group; otherwise, <b>FALSE</b>.




## -remarks



This function is a wrapper for <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a>. It is recommended to call that function directly to determine Administrator group status rather than calling  <b>IsUserAnAdmin</b>.




## -see-also




<a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a>
 

 

