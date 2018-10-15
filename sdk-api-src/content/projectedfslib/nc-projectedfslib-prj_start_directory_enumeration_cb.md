---
UID: NC:projectedfslib.PRJ_START_DIRECTORY_ENUMERATION_CB
title: PRJ_START_DIRECTORY_ENUMERATION_CB
author: windows-sdk-content
description: Informs the provider that a directory enumeration is starting.
old-location: projfs\prj_start_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: 09F284D4-BF39-42C9-A89B-DDC8201362EE
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PRJ_START_DIRECTORY_ENUMERATION_CB, PRJ_START_DIRECTORY_ENUMERATION_CB callback, PRJ_START_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_start_directory_enumeration_cb, projectedfslib/PRJ_START_DIRECTORY_ENUMERATION_CB
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
 - PRJ_START_DIRECTORY_ENUMERATION_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_START_DIRECTORY_ENUMERATION_CB callback function


## -description


Informs the provider that a directory enumeration is starting.


## -parameters




### -param callbackData [in]

Information about the operation. The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it. 


### -param enumerationId [in]

An identifier for this enumeration session.


## -returns



S_OK: 
The provider successfully completed the operation. 


HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND): The directory to be enumerated does not exist in the provider’s backing store. 


HRESULT_FROM_WIN32(ERROR_IO_PENDING): 
The provider wishes to complete the operation at a later time. 


An appropriate HRESULT error code if the provider fails the operation.




## -remarks



ProjFS requests a directory enumeration from the provider by first invoking this callback, then one or more <a href="projfs.prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callbacks, then the <a href="projfs.prj_end_directory_enumeration_cb">PRJ_END_DIRECTORY_ENUMERATION_CB</a> callback. Because multiple enumerations may occur in parallel in the same location, ProjFS uses the enumerationId argument to associate the callback invocations into a single enumeration session, meaning that a given set of calls to the enumeration callbacks will use the same value for enumerationId for the same session.



