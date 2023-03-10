---
UID: NF:setupapi.SetupTermDefaultQueueCallback
title: SetupTermDefaultQueueCallback function (setupapi.h)
description: The SetupTermDefaultQueueCallback function is called after a queue has finished committing. It frees resources allocated by previous calls to SetupInitDefaultQueueCallback or SetupInitDefaultQueueCallbackEx.
helpviewer_keywords: ["SetupTermDefaultQueueCallback","SetupTermDefaultQueueCallback function [Setup API]","_setupapi_setuptermdefaultqueuecallback","setup.setuptermdefaultqueuecallback","setupapi/SetupTermDefaultQueueCallback"]
old-location: setup\setuptermdefaultqueuecallback.htm
tech.root: setup
ms.assetid: de99ee40-9fbb-42e2-b070-d1c25b238135
ms.date: 12/05/2018
ms.keywords: SetupTermDefaultQueueCallback, SetupTermDefaultQueueCallback function [Setup API], _setupapi_setuptermdefaultqueuecallback, setup.setuptermdefaultqueuecallback, setupapi/SetupTermDefaultQueueCallback
req.header: setupapi.h
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupTermDefaultQueueCallback
 - setupapi/SetupTermDefaultQueueCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupTermDefaultQueueCallback
---

# SetupTermDefaultQueueCallback function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupTermDefaultQueueCallback</b> function is called after a queue has finished committing. It frees resources allocated by previous calls to 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallback">SetupInitDefaultQueueCallback</a> or 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallbackex">SetupInitDefaultQueueCallbackEx</a>.

## -parameters

### -param Context [in]

Pointer to the context used by the default callback routine.

## -returns

Does not return a value.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Regardless of whether you initialized the context used by the default queue callback routine with 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallback">SetupInitDefaultQueueCallback</a> or 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallbackex">SetupInitDefaultQueueCallbackEx</a>, after the queued operations have finished processing, call 
<b>SetupTermDefaultQueueCallback</b> to release the resources allocated in initializing the context structure. For more information see 
<a href="/windows/desktop/SetupApi/initializing-and-terminating-the-callback-context">Initializing and Terminating the Callback Context</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallback">SetupInitDefaultQueueCallback</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallbackex">SetupInitDefaultQueueCallbackEx</a>