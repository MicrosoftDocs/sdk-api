---
UID: NS:winnt._UMS_CREATE_THREAD_ATTRIBUTES
title: UMS_CREATE_THREAD_ATTRIBUTES (winnt.h)
description: Specifies attributes for a user-mode scheduling (UMS) worker thread.
helpviewer_keywords: ["*PUMS_CREATE_THREAD_ATTRIBUTES","PUMS_CREATE_THREAD_ATTRIBUTES","PUMS_CREATE_THREAD_ATTRIBUTES structure pointer","UMS_CREATE_THREAD_ATTRIBUTES","UMS_CREATE_THREAD_ATTRIBUTES structure","_UMS_CREATE_THREAD_ATTRIBUTES","base.ums_create_thread_attributes","winnt/PUMS_CREATE_THREAD_ATTRIBUTES","winnt/UMS_CREATE_THREAD_ATTRIBUTES"]
old-location: base\ums_create_thread_attributes.htm
tech.root: backup
ms.assetid: 5d3e1721-c439-49bb-9cb6-8386fa8aaf50
ms.date: 12/05/2018
ms.keywords: '*PUMS_CREATE_THREAD_ATTRIBUTES, PUMS_CREATE_THREAD_ATTRIBUTES, PUMS_CREATE_THREAD_ATTRIBUTES structure pointer, UMS_CREATE_THREAD_ATTRIBUTES, UMS_CREATE_THREAD_ATTRIBUTES structure, _UMS_CREATE_THREAD_ATTRIBUTES, base.ums_create_thread_attributes, winnt/PUMS_CREATE_THREAD_ATTRIBUTES, winnt/UMS_CREATE_THREAD_ATTRIBUTES'
req.header: winnt.h
req.include-header: 
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
req.typenames: UMS_CREATE_THREAD_ATTRIBUTES, *PUMS_CREATE_THREAD_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UMS_CREATE_THREAD_ATTRIBUTES
 - winnt/_UMS_CREATE_THREAD_ATTRIBUTES
 - PUMS_CREATE_THREAD_ATTRIBUTES
 - winnt/PUMS_CREATE_THREAD_ATTRIBUTES
 - UMS_CREATE_THREAD_ATTRIBUTES
 - winnt/UMS_CREATE_THREAD_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - UMS_CREATE_THREAD_ATTRIBUTES
---

# UMS_CREATE_THREAD_ATTRIBUTES structure


## -description

Specifies attributes for a user-mode scheduling (UMS) worker thread. 

This structure is used with the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a> function.

## -struct-fields

### -field UmsVersion

The UMS version for which the application was built. This parameter must be <b>UMS_VERSION</b>.

### -field UmsContext

A pointer to a UMS thread context for the worker thread to be created. This pointer is provided by the <a href="/windows/desktop/api/winbase/nf-winbase-createumsthreadcontext">CreateUmsThreadContext</a> function.

### -field UmsCompletionList

A pointer to a UMS completion list. This pointer is provided by the <a href="/windows/desktop/api/winbase/nf-winbase-createumscompletionlist">CreateUmsCompletionList</a> function. The newly created worker thread is queued to the specified completion list.