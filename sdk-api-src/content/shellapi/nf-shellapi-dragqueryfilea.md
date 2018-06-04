---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DragQueryFileA function


## -description


Retrieves the names of dropped files that result from a successful drag-and-drop operation.


## -parameters




### -param hDrop [in]

Type: <b>HDROP</b>

Identifier of the structure that contains the file names of the dropped files.


### -param iFile [in]

Type: <b>UINT</b>

Index of the file to query. If the value of this parameter is 0xFFFFFFFF, <b>DragQueryFile</b> returns a count of the files dropped. If the value of this parameter is between zero and the total number of files dropped, <b>DragQueryFile</b> copies the file name with the corresponding value to the buffer pointed to by the <i>lpszFile</i> parameter.


### -param lpszFile [out]

Type: <b>LPTSTR</b>

The address of a buffer that receives the file name of a dropped file when the function returns. This file name is a null-terminated string. If this parameter is <b>NULL</b>, <b>DragQueryFile</b> returns the required size, in characters, of this buffer.


### -param cch

Type: <b>UINT</b>

The size, in characters, of the <i>lpszFile</i> buffer.


## -returns



Type: <b>UINT</b>

A nonzero value indicates a successful call.

When the function copies a file name to the buffer, the return value is a count of the characters copied, not including the terminating null character.

If the index value is 0xFFFFFFFF, the return value is a count of the dropped files. Note that the index variable itself returns unchanged, and therefore remains 0xFFFFFFFF.

If the index value is between zero and the total number of dropped files, and the <i>lpszFile</i> buffer address is <b>NULL</b>, the return value is the required size, in characters, of the buffer, <i>not including</i> the terminating null character.




## -see-also




<a href="https://msdn.microsoft.com/87794ab0-a075-4a1f-869f-5998bdc57a1d">DragQueryPoint</a>
 

 

