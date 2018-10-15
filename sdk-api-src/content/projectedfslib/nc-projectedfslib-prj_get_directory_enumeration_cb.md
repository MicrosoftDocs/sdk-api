---
UID: NC:projectedfslib.PRJ_GET_DIRECTORY_ENUMERATION_CB
title: PRJ_GET_DIRECTORY_ENUMERATION_CB
author: windows-sdk-content
description: Requests directory enumeration information from the provider.
old-location: projfs\prj_get_directory_enumeration_cb.htm
tech.root: ProjFS
ms.assetid: 45E7E7F9-9E54-44C8-9915-43CCECF85DB6
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PRJ_GET_DIRECTORY_ENUMERATION_CB, PRJ_GET_DIRECTORY_ENUMERATION_CB callback, PRJ_GET_DIRECTORY_ENUMERATION_CB callback function, ProjFS.prj_get_directory_enumeration_cb, projectedfslib/PRJ_GET_DIRECTORY_ENUMERATION_CB
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - PRJ_GET_DIRECTORY_ENUMERATION_CB callback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_GET_DIRECTORY_ENUMERATION_CB callback function


## -description


Requests directory enumeration information from the provider.


## -parameters




### -param callbackData [in]

Information about the operation.


### -param enumerationId [in]

TBD


### -param searchExpression [in, optional]

A pointer to a null-terminated Unicode string specifying a search expression. The search expression may include wildcard characters.


### -param dirEntryBufferHandle [in]

An opaque handle to a structure that receives the results of the enumeration from the provider. The provider uses the <a href="projfs.prjfilldirentrybuffer">PrjFillDirEntryBuffer</a> routine to fill the structure.


## -returns



S_OK: 
The provider successfully added at least one entry to dirEntryBufferHandle, or no entries in the provider’s store match searchExpression. 


HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER): The provider received this error from <a href="projfs.prjfilldirentrybuffer">PrjFillDirEntryBuffer</a> for the first file or directory it tried to add to dirEntryBufferHandle. 


HRESULT_FROM_WIN32(ERROR_IO_PENDING): 
The provider wishes to complete the operation at a later time. 


An appropriate HRESULT error code if the provider fails the operation.




## -remarks



The provider should use the PrjDoesNameContainWildCards routine to determine whether wildcards are present in searchExpression, and it should use the PrjFileNameMatch routine to determine whether an entry in its backing store matches a search expression containing wildcards. 


This parameter is optional and may be NULL. 
<ul>
<li>If this parameter is not NULL, the provider must return only those directory entries whose names match the search expression.</li>
<li>If this parameter is NULL, the provider must return all directory entries.</li>
</ul>The provider should capture the value of this parameter on the first invocation of this callback for an enumeration session and use it on subsequent invocations, ignoring this parameter on those invocations unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is specified in the Flags member of callbackData. In that case the provider must re-capture the value of searchExpression. 



