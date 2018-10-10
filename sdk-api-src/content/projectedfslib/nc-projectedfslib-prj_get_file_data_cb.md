---
UID: NC:projectedfslib.PRJ_GET_FILE_DATA_CB
title: PRJ_GET_FILE_DATA_CB
author: windows-sdk-content
description: Requests the contents of a file's primary data stream.
old-location: projfs\prj_get_file_data_cb.htm
tech.root: ProjFS
ms.assetid: 8F3EEC96-70C2-40ED-BDF3-B6E979EF1F7E
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRJ_GET_FILE_DATA_CB, PRJ_GET_FILE_DATA_CB callback, PRJ_GET_FILE_DATA_CB callback function, ProjFS.prj_get_file_data_cb, projectedfslib/PRJ_GET_FILE_DATA_CB
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
 - PRJ_GET_FILE_DATA_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_GET_FILE_DATA_CB callback function


## -description


Requests the contents of a file's primary data stream.


## -parameters




### -param callbackData [in]

Information about the operation.


### -param byteOffset [in]

Offset of the requested data, in bytes, from the beginning of the file. The provider must return file data starting at or before this offset


### -param length [in]

Number of bytes of file data requested. The provider must return at least this many bytes of file data beginning with byteOffset.


## -returns



S_OK: The provider successfully returned all the requested data. 


HRESULT_FROM_WIN32(ERROR_IO_PENDING): 
The provider wishes to complete the operation at a later time. 


An appropriate HRESULT error code if the provider fails the operation.




## -remarks



When ProjFS receives the data it will write it to the file to convert it into a hydrated placeholder. 


To handle this callback, the provider issues one or more calls to <a href="projfs.prjwritefiledata">PrjWriteFileData</a> to give ProjFS the requested contents of the file's primary data stream. Then the provider completes the callback. 



