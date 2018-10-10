---
UID: NC:projectedfslib.PRJ_END_DIRECTORY_ENUMERATION_CB
title: PRJ_END_DIRECTORY_ENUMERATION_CB
author: windows-sdk-content
description: Informs the provider that a directory enumeration is over.
old-location: projfs\prj_end_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: E9DA86AC-E884-4DB3-977D-6D8EDA2A8E12
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRJ_END_DIRECTORY_ENUMERATION_CB, PRJ_END_DIRECTORY_ENUMERATION_CB callback, PRJ_END_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_end_directory_enumeration_cb, projectedfslib/PRJ_END_DIRECTORY_ENUMERATION_CB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ProjectedFSLib.h
api_name:
 - PRJ_END_DIRECTORY_ENUMERATION_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_END_DIRECTORY_ENUMERATION_CB callback function


## -description


Informs the provider that a directory enumeration is over.


## -parameters




### -param callbackData [in]

Information about the operation. 


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.


### -param enumerationId [in]

An identifier for this enumeration session.


## -returns



S_OK: The provider successfully completed the operation.

HRESULT_FROM_WIN32(ERROR_IO_PENDING): The provider wishes to complete the operation at a later time.

The provider should not return any other value from this callback.




## -remarks



For a user-initiated enumeration ProjFS invokes this callback when the file handle used to enumerate the directory is closed. For a ProjFS-initiated enumeration, this callback is invoked when ProjFS completes the enumeration.



