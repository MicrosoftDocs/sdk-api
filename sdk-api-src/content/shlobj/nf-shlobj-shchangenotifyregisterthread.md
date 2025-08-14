---
UID: NF:shlobj.SHChangeNotifyRegisterThread
title: SHChangeNotifyRegisterThread function (shlobj.h)
description: Enables asynchronous register and deregister of a thread.
helpviewer_keywords: ["SHChangeNotifyRegisterThread","SHChangeNotifyRegisterThread function [Windows Shell]","_shell_SHChangeNotifyRegisterThread","shell.SHChangeNotifyRegisterThread","shlobj/SHChangeNotifyRegisterThread"]
old-location: shell\SHChangeNotifyRegisterThread.htm
tech.root: shell
ms.assetid: 170afefc-b4de-4661-9c12-1341656b0fdb
ms.date: 12/05/2018
ms.keywords: SHChangeNotifyRegisterThread, SHChangeNotifyRegisterThread function [Windows Shell], _shell_SHChangeNotifyRegisterThread, shell.SHChangeNotifyRegisterThread, shlobj/SHChangeNotifyRegisterThread
req.header: shlobj.h
req.include-header: 
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHChangeNotifyRegisterThread
 - shlobj/SHChangeNotifyRegisterThread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shell-changenotify-l1-1-1.dll
 - Shell32.dll
api_name:
 - SHChangeNotifyRegisterThread
---

# SHChangeNotifyRegisterThread function


## -description

Enables asynchronous register and deregister of a thread.

## -parameters

### -param status

Type: <b><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status">SCNRT_STATUS</a></b>

Indicates whether the function is being used to register or deregister the thread. One of the values of <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status">SCNRT_STATUS</a>.