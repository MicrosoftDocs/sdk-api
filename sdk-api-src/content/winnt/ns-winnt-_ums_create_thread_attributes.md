---
UID: NS:winnt._UMS_CREATE_THREAD_ATTRIBUTES
title: "_UMS_CREATE_THREAD_ATTRIBUTES"
author: windows-sdk-content
description: Specifies attributes for a user-mode scheduling (UMS) worker thread.
old-location: base\ums_create_thread_attributes.htm
tech.root: procthread
ms.assetid: 5d3e1721-c439-49bb-9cb6-8386fa8aaf50
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PUMS_CREATE_THREAD_ATTRIBUTES, PUMS_CREATE_THREAD_ATTRIBUTES, PUMS_CREATE_THREAD_ATTRIBUTES structure pointer, UMS_CREATE_THREAD_ATTRIBUTES, UMS_CREATE_THREAD_ATTRIBUTES structure, _UMS_CREATE_THREAD_ATTRIBUTES, base.ums_create_thread_attributes, winnt/PUMS_CREATE_THREAD_ATTRIBUTES, winnt/UMS_CREATE_THREAD_ATTRIBUTES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - UMS_CREATE_THREAD_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: UMS_CREATE_THREAD_ATTRIBUTES, *PUMS_CREATE_THREAD_ATTRIBUTES
req.redist: 
---

# _UMS_CREATE_THREAD_ATTRIBUTES structure


## -description


Specifies attributes for a user-mode scheduling (UMS) worker thread. 

This structure is used with the <a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a> function.  


## -struct-fields




### -field UmsVersion

The UMS version for which the application was built. This parameter must be <b>UMS_VERSION</b>. 


### -field UmsContext

A pointer to a UMS thread context for the worker thread to be created. This pointer is provided by the <a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a> function.


### -field UmsCompletionList

A pointer to a UMS completion list. This pointer is provided by the <a href="https://msdn.microsoft.com/6e77b793-a82e-4e23-8c8b-7aff79d69346">CreateUmsCompletionList</a> function. The newly created worker thread is queued to the specified completion list.

