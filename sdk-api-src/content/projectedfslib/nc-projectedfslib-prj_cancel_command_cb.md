---
UID: NC:projectedfslib.PRJ_CANCEL_COMMAND_CB
title: PRJ_CANCEL_COMMAND_CB
author: windows-sdk-content
description: Notifies the provider that an operation by an earlier invocation of a callback should be canceled.
old-location: projfs\prj_cancel_command_cb.htm
tech.root: ProjFS
ms.assetid: 8C646A8C-7C55-4F54-965A-04ACAC64C65D
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PRJ_CANCEL_COMMAND_CB, PRJ_CANCEL_COMMAND_CB callback, PRJ_CANCEL_COMMAND_CB callback function, ProjFS.prj_cancel_command_cb, projectedfslib/PRJ_CANCEL_COMMAND_CB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_CANCEL_COMMAND_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_CANCEL_COMMAND_CB callback function


## -description


Notifies the provider that an operation by an earlier invocation of a callback should be canceled.


## -parameters




### -param callbackData [in]

Information about the operation.


## -returns



None




## -remarks



Every invocation of a provider callback has a callbackData parameter with a CommandId field. If a provider supplies an implementation of this callback, it should keep track of the CommandId values of callbacks that it processes asynchronously, i.e. callbacks from which it has returned HRESULT_FROM_WIN32(ERROR_IO_PENDING) but not yet completed by calling PrjCompleteCommand. If the provider receives this callback, it indicates that the I/O that caused the earlier callback to be invoked was canceled, either explicitly or because the thread it was issued on terminated. The provider should cancel processing the callback invocation identified by CommandId as soon as possible. 


Calling <a href="projfs.prjcompletecommand">PrjCompleteCommand</a> for the CommandId in this callback's callbackData is not an error, however it is a no-op because the I/O that caused the callback invocation identified by CommandId has already ended. 


ProjFS will invoke <i>PRJ_CANCEL_COMMAND_CB</i> for a given CommandId only after the callback to be canceled is invoked. However if the provider is configured to allow more than one concurrently running worker thread, the cancellation and original invocation may run concurrently. The provider must be able to handle this situation.

 
This callback is optional. If the provider does not supply an implementation of this callback, none of the other callbacks will be cancellable. The provider will process all callbacks synchronously.



