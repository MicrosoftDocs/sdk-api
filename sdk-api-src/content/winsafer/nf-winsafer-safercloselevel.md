---
UID: NF:winsafer.SaferCloseLevel
title: SaferCloseLevel function (winsafer.h)
author: windows-sdk-content
description: Closes a SAFER_LEVEL_HANDLE that was opened by using the SaferIdentifyLevel function or the SaferCreateLevel function.
old-location: security\safercloselevel.htm
tech.root: SecMgmt
ms.assetid: 8daffb35-5bb0-45b3-aff1-a8ea6a142ba5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SaferCloseLevel, SaferCloseLevel function [Security], _mnp_safercloselevel, security.safercloselevel, winsafer/SaferCloseLevel
ms.topic: function
req.header: winsafer.h
req.include-header: 
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
 - SaferCloseLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SaferCloseLevel function


## -description


The <b>SaferCloseLevel</b> function closes a SAFER_LEVEL_HANDLE that was opened by using the  
<a href="https://docs.microsoft.com/windows/desktop/api/winsafer/nf-winsafer-saferidentifylevel">SaferIdentifyLevel</a> function or 
the <a href="https://docs.microsoft.com/windows/desktop/api/winsafer/nf-winsafer-safercreatelevel">SaferCreateLevel</a> function.


## -parameters




### -param hLevelHandle [in]

The SAFER_LEVEL_HANDLE to be closed.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



