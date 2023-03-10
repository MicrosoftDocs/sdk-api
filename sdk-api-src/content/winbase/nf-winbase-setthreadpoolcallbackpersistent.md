---
UID: NF:winbase.SetThreadpoolCallbackPersistent
title: SetThreadpoolCallbackPersistent function (winbase.h)
description: Specifies that the callback should run on a persistent thread. (SetThreadpoolCallbackPersistent)
helpviewer_keywords: ["SetThreadpoolCallbackPersistent","SetThreadpoolCallbackPersistent function","base.setthreadpoolcallbackpersistent","winbase/SetThreadpoolCallbackPersistent"]
old-location: base\setthreadpoolcallbackpersistent.htm
tech.root: backup
ms.assetid: 3f209586-5452-4928-8f97-70648b22460d
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackPersistent, SetThreadpoolCallbackPersistent function, base.setthreadpoolcallbackpersistent, winbase/SetThreadpoolCallbackPersistent
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadpoolCallbackPersistent
 - winbase/SetThreadpoolCallbackPersistent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackPersistent
---

# SetThreadpoolCallbackPersistent function


## -description

Specifies that the callback should run on a persistent thread.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

## -remarks

This function is implemented as an inline function.

To compile an application that uses this function, set _WIN32_WINNT to _WIN32_WINNT_WIN7. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.
