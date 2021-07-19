---
UID: NF:setupapi.SetupOpenFileQueue
title: SetupOpenFileQueue function (setupapi.h)
description: The SetupOpenFileQueue function creates a setup file queue.
helpviewer_keywords: ["SetupOpenFileQueue","SetupOpenFileQueue function [Setup API]","_setupapi_setupopenfilequeue","setup.setupopenfilequeue","setupapi/SetupOpenFileQueue"]
old-location: setup\setupopenfilequeue.htm
tech.root: setup
ms.assetid: 36950f18-80ae-46b7-9f9f-bd5307d72a3b
ms.date: 12/05/2018
ms.keywords: SetupOpenFileQueue, SetupOpenFileQueue function [Setup API], _setupapi_setupopenfilequeue, setup.setupopenfilequeue, setupapi/SetupOpenFileQueue
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
 - SetupOpenFileQueue
 - setupapi/SetupOpenFileQueue
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
 - SetupOpenFileQueue
---

# SetupOpenFileQueue function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenFileQueue</b> function creates a setup file queue.



## -returns

If the function succeeds, it returns a handle to a setup file queue. If there is not enough memory to create the queue, the function returns INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After the file queue has been committed and is no longer needed, 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a> should be called to release the resources allocated during 
<b>SetupOpenFileQueue</b>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfilea">SetupInstallFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamea">SetupQueueRename</a>
