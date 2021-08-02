---
UID: NC:projectedfslib.PRJ_CANCEL_COMMAND_CB
title: PRJ_CANCEL_COMMAND_CB (projectedfslib.h)
description: Notifies the provider that an operation by an earlier invocation of a callback should be canceled.
helpviewer_keywords: ["PRJ_CANCEL_COMMAND_CB","PRJ_CANCEL_COMMAND_CB callback","PRJ_CANCEL_COMMAND_CB callback function","ProjFS.prj_cancel_command_cb","projectedfslib/PRJ_CANCEL_COMMAND_CB"]
old-location: projfs\prj_cancel_command_cb.htm
tech.root: ProjFS
ms.assetid: 8C646A8C-7C55-4F54-965A-04ACAC64C65D
ms.date: 12/05/2018
ms.keywords: PRJ_CANCEL_COMMAND_CB, PRJ_CANCEL_COMMAND_CB callback, PRJ_CANCEL_COMMAND_CB callback function, ProjFS.prj_cancel_command_cb, projectedfslib/PRJ_CANCEL_COMMAND_CB
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_CANCEL_COMMAND_CB
 - projectedfslib/PRJ_CANCEL_COMMAND_CB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_CANCEL_COMMAND_CB
---

# PRJ_CANCEL_COMMAND_CB callback function


## -description

Notifies the provider that an operation by an earlier invocation of a callback should be canceled.

## -parameters

### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>CommandId</b> Identifies the operation to be cancelled.

</dd>
</dl>

## -remarks

Every invocation of a provider callback has a <i>callbackData</i> parameter with a <b>CommandId</b> field. If a provider supplies an implementation of this callback, it should keep track of the <b>CommandId</b> values of callbacks that it processes asynchronously, i.e. callbacks from which it has returned <b>HRESULT_FROM_WIN32(ERROR_IO_PENDING)</b> but not yet completed by calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand">PrjCompleteCommand</a>. If the provider receives this callback, it indicates that the I/O that caused the earlier callback to be invoked was canceled, either explicitly or because the thread it was issued on terminated. The provider should cancel processing the callback invocation identified by <b>CommandId</b> as soon as possible. 


Calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand">PrjCompleteCommand</a> for the <b>CommandId</b> in this callback's callbackData is not an error, however it is a no-op because the I/O that caused the callback invocation identified by <b>CommandId</b> has already ended. 


ProjFS will invoke <i>PRJ_CANCEL_COMMAND_CB</i> for a given <b>CommandId</b> only after the callback to be canceled is invoked. However if the provider is configured to allow more than one concurrently running worker thread, the cancellation and original invocation may run concurrently. The provider must be able to handle this situation.

 
This callback is optional. If the provider does not supply an implementation of this callback, none of the other callbacks will be cancellable. The provider will process all callbacks synchronously.