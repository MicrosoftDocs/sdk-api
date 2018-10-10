---
UID: NC:projectedfslib.PRJ_QUERY_FILE_NAME_CB
title: PRJ_QUERY_FILE_NAME_CB
author: windows-sdk-content
description: Determines whether a given file path exists in the provider's backing store.
old-location: projfs\prj_query_file_name_cb.htm
tech.root: ProjFS
ms.assetid: 1B218D41-AF24-48C2-9E11-7E0455CE15AC
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRJ_QUERY_FILE_NAME_CB, PRJ_QUERY_FILE_NAME_CB callback, PRJ_QUERY_FILE_NAME_CB callback function, ProjFS.prj_query_file_name_cb, projectedfslib/PRJ_QUERY_FILE_NAME_CB
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
 - PRJ_QUERY_FILE_NAME_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_QUERY_FILE_NAME_CB callback function


## -description


Determines whether a given file path exists in the provider's backing store.


## -parameters




### -param callbackData [in]

Information about the operation.


## -returns



S_OK: The queried file path exists in the provider's store. 


HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND): The queried file path does not exist in the provider's store. 


HRESULT_FROM_WIN32(ERROR_IO_PENDING): 
The provider wishes to complete the operation at a later time. 


An appropriate HRESULT error code if the provider fails the operation.



