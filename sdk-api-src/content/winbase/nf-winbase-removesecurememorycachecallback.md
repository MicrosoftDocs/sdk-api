---
UID: NF:winbase.RemoveSecureMemoryCacheCallback
title: RemoveSecureMemoryCacheCallback function (winbase.h)
description: Unregisters a callback function that was previously registered with the AddSecureMemoryCacheCallback function.
helpviewer_keywords: ["RemoveSecureMemoryCacheCallback","RemoveSecureMemoryCacheCallback function","base.removesecurememorycachecallback","winbase/RemoveSecureMemoryCacheCallback"]
old-location: base\removesecurememorycachecallback.htm
tech.root: base
ms.assetid: 8be6ff04-34c7-4942-a38c-507584c8bbeb
ms.date: 12/05/2018
ms.keywords: RemoveSecureMemoryCacheCallback, RemoveSecureMemoryCacheCallback function, base.removesecurememorycachecallback, winbase/RemoveSecureMemoryCacheCallback
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemoveSecureMemoryCacheCallback
 - winbase/RemoveSecureMemoryCacheCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - RemoveSecureMemoryCacheCallback
---

# RemoveSecureMemoryCacheCallback function


## -description

Unregisters a callback function that was previously registered with the <a href="/windows/desktop/api/winbase/nf-winbase-addsecurememorycachecallback">AddSecureMemoryCacheCallback</a> function.

## -parameters

### -param pfnCallBack [in]

A pointer to the application-defined <a href="/windows/desktop/api/winnt/nc-winnt-psecure_memory_cache_callback">SecureMemoryCacheCallback</a> function to remove.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addsecurememorycachecallback">AddSecureMemoryCacheCallback</a>



<a href="/windows/desktop/api/winnt/nc-winnt-psecure_memory_cache_callback">SecureMemoryCacheCallback</a>