---
UID: NF:setupapi.SetupOpenFileQueue
title: SetupOpenFileQueue function (setupapi.h)
description: The SetupOpenFileQueue function creates a setup file queue.
old-location: setup\setupopenfilequeue.htm
tech.root: SetupApi
ms.assetid: 36950f18-80ae-46b7-9f9f-bd5307d72a3b
ms.date: 12/05/2018
ms.keywords: SetupOpenFileQueue, SetupOpenFileQueue function [Setup API], _setupapi_setupopenfilequeue, setup.setupopenfilequeue, setupapi/SetupOpenFileQueue
ms.topic: function
f1_keywords:
- setupapi/SetupOpenFileQueue
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Setupapi.dll
api_name:
- SetupOpenFileQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupOpenFileQueue function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenFileQueue</b> function creates a setup file queue.


## -parameters






## -returns



If the function succeeds, it returns a handle to a setup file queue. If there is not enough memory to create the queue, the function returns INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



After the file queue has been committed and is no longer needed, 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a> should be called to release the resources allocated during 
<b>SetupOpenFileQueue</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupinstallfilea">SetupInstallFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuedeletea">SetupQueueDelete</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuerenamea">SetupQueueRename</a>
 

 

