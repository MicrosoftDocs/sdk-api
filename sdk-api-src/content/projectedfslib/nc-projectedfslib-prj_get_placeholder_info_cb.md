---
UID: NC:projectedfslib.PRJ_GET_PLACEHOLDER_INFO_CB
title: PRJ_GET_PLACEHOLDER_INFO_CB
author: windows-sdk-content
description: Requests information for a file or directory from the provider.
old-location: projfs\prj_get_placeholder_info_cb.htm
tech.root: ProjFS
ms.assetid: 1BC7C1FA-1BAB-48FB-85C2-34EC3B1B4167
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRJ_GET_PLACEHOLDER_INFO_CB, PRJ_GET_PLACEHOLDER_INFO_CB callback, PRJ_GET_PLACEHOLDER_INFO_CB callback function, ProjFS.prj_get_placeholder_info_cb, projectedfslib/PRJ_GET_PLACEHOLDER_INFO_CB
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
 - PRJ_GET_PLACEHOLDER_INFO_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_GET_PLACEHOLDER_INFO_CB callback function


## -description


Requests information for a file or directory from the provider.


## -parameters




### -param callbackData [in]

Information about the operation.


## -returns



S_OK: The file exists in the provider's store and it successfully gave the file's information to ProjFS. 


HRESULT_FROM_WIN32(ERROR_IO_PENDING): 
The provider wishes to complete the operation at a later time. 


HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND): 
The file does not exist in the provider's store. 


Another appropriate HRESULT error code if the provider fails the operation. 




## -remarks



ProjFS will use the information provided in this callback to create a placeholder for the requested item. 


To handle this callback, the provider calls <a href="projfs.prjwriteplaceholderinfo">PrjWritePlaceholderInfo</a> to give ProjFS the information for the requested file name. Then the provider completes the callback.



