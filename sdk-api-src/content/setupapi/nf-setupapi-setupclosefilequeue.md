---
UID: NF:setupapi.SetupCloseFileQueue
title: SetupCloseFileQueue function (setupapi.h)
description: The SetupCloseFileQueue function destroys a setup file queue.
helpviewer_keywords: ["SetupCloseFileQueue","SetupCloseFileQueue function [Setup API]","_setupapi_setupclosefilequeue","setup.setupclosefilequeue","setupapi/SetupCloseFileQueue"]
old-location: setup\setupclosefilequeue.htm
tech.root: setup
ms.assetid: 51c63e65-a844-46b4-93ef-8a92a9c8a604
ms.date: 12/05/2018
ms.keywords: SetupCloseFileQueue, SetupCloseFileQueue function [Setup API], _setupapi_setupclosefilequeue, setup.setupclosefilequeue, setupapi/SetupCloseFileQueue
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
 - SetupCloseFileQueue
 - setupapi/SetupCloseFileQueue
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
 - SetupCloseFileQueue
---

# SetupCloseFileQueue function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCloseFileQueue</b> function destroys a setup file queue.

## -parameters

### -param QueueHandle [in]

Handle to an open setup file queue.

## -returns

This function does not return a value.

## -remarks

The 
<b>SetupCloseFileQueue</b> function does not flush the queue; pending operations are not performed. To commit a file queue before closing it call 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinstallfilea">SetupInstallFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedefaultcopya">SetupQueueDefaultCopy</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamea">SetupQueueRename</a>