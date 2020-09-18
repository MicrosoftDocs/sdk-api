---
UID: NC:winbio.PWINBIO_ASYNC_COMPLETION_CALLBACK
title: PWINBIO_ASYNC_COMPLETION_CALLBACK (winbio.h)
description: Notifies the client application that an asynchronous operation started by using WinBioAsyncOpenSession or WinBioAsyncOpenFramework has completed.
helpviewer_keywords: ["PWINBIO_ASYNC_COMPLETION_CALLBACK","PWINBIO_ASYNC_COMPLETION_CALLBACK function","PWINBIO_ASYNC_COMPLETION_CALLBACK function pointer [Windows Biometric Framework API]","secbiomet.pwinbio_async_completion_callback","winbio/PWINBIO_ASYNC_COMPLETION_CALLBACK"]
old-location: secbiomet\pwinbio_async_completion_callback.htm
tech.root: SecBioMet
ms.assetid: 550EA13D-18CE-4B73-9C9B-4D5C46C48A75
ms.date: 12/05/2018
ms.keywords: PWINBIO_ASYNC_COMPLETION_CALLBACK, PWINBIO_ASYNC_COMPLETION_CALLBACK function, PWINBIO_ASYNC_COMPLETION_CALLBACK function pointer [Windows Biometric Framework API], secbiomet.pwinbio_async_completion_callback, winbio/PWINBIO_ASYNC_COMPLETION_CALLBACK
req.header: winbio.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWINBIO_ASYNC_COMPLETION_CALLBACK
 - winbio/PWINBIO_ASYNC_COMPLETION_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio.h
api_name:
 - PWINBIO_ASYNC_COMPLETION_CALLBACK
---

# PWINBIO_ASYNC_COMPLETION_CALLBACK callback function


## -description

Called by the Windows Biometric Framework to notify the client application that an asynchronous operation has completed. The callback is defined by the client application and called by the Windows Biometric Framework.

## -parameters

### -param AsyncResult [in]

Pointer to a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure that contains information about the completed operation. The structure is created by the Windows Biometric Framework. You must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the structure.

## -remarks

You must create this callback if you open a biometric session by using the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> function or the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a> function and you set  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter of either function.

<div class="alert"><b>Important</b>  The <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure is allocated internally by the Windows Biometric Framework. Therefore, when you are through using it, call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the allocated memory and avoid leaks. Because this also releases all nested data structures, you should not keep a copy of any pointers returned in the <b>WINBIO_ASYNC_RESULT</b> structure. If you want to save any data returned in a nested structure, make a private copy of that data before calling <b>WinBioFree</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>