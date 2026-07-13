---
UID: NN:shlobj.ICopyHookA
title: ICopyHookA
description: Exposes a method that creates a copy hook handler. (ANSI)
helpviewer_keywords: ["ICopyHookA"]
old-location: 
tech.root: shell
ms.assetid: c3ffa682-250f-458b-8ad5-b25871b3901b
ms.date: 01/30/2019
ms.keywords: ICopyHookA
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: shlobj.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
f1_keywords:
 - ICopyHookA
 - shlobj/ICopyHookA
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - ICopyHookA
---

## -description

Exposes a method that creates a *copy hook handler*. A copy hook handler is a Shell extension that determines if a Shell folder or printer object can be moved, copied, renamed, or deleted. The Shell calls the [ICopyHookA::CopyCallback](nf-shlobj-icopyhooka-copycallback.md) method prior to performing one of these operations.

## -inheritance

## -remarks

The copy hook handler, which is an OLE in-process server (a dll), does not perform the task itself, but it does approve or disapprove the action. If the Shell receives approval from the copy hook handler, it performs the file system operation. Copy hook handlers are not informed about the success of an operation, so they cannot monitor actions taken on folder objects unless [FindFirstChangeNotification](/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa) is used.

A folder object can have multiple copy hook handlers. For example, even if the Shell already has a copy hook handler registered for a particular folder object, you can still register one of your own. If two or more copy hook handlers are registered for an object, the Shell simply calls each of them before performing one of the specified file system operations.

The Shell initializes **ICopyHookA** directly, without using the [IShellExtInit](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.

[CopyCallback](nf-shlobj-icopyhooka-copycallback.md) returns an int value that indicates whether the Shell should perform the operation. The Shell will call each copy hook handler registered for a folder object until all the handlers have been called or until one of them has returned a value other than IDYES. The handler returns IDYES to specify that the operation should be performed, or IDNO or IDCANCEL to specify that the operation should be discontinued.

Implement a copy hook handler when you want to be able to control when, or if, these file system operations are performed on a given object. You might want to use a copy hook handler on shared folders, for example.

You do not call this Shell extension directly. [CopyCallback](nf-shlobj-icopyhooka-copycallback.md) is called by the Shell prior to moving, copying, deleting, or renaming a Shell folder object.
		


> [!NOTE]
> The shlobj.h header defines ICopyHook as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also
