---
UID: NF:winuser.IsImmersiveProcess
title: IsImmersiveProcess function (winuser.h)
description: Determines whether the process belongs to a Windows Store app.
helpviewer_keywords: ["IsImmersiveProcess","IsImmersiveProcess function","base.isimmersiveprocess","winuser/IsImmersiveProcess"]
old-location: base\isimmersiveprocess.htm
tech.root: backup
ms.assetid: E95FD9C0-8E4A-44FA-BBA6-0A7F53A0E584
ms.date: 12/05/2018
ms.keywords: IsImmersiveProcess, IsImmersiveProcess function, base.isimmersiveprocess, winuser/IsImmersiveProcess
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsImmersiveProcess
 - winuser/IsImmersiveProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-uicontext-Ext-l1-1-0.dll
 - modernapiexthost.dll
 - api-ms-win-ntuser-uicontext-l1-1-0.dll
api_name:
 - IsImmersiveProcess
---

# IsImmersiveProcess function


## -description

Determines whether the process belongs to a Windows Store app.

## -parameters

### -param hProcess [in]

Target process handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.