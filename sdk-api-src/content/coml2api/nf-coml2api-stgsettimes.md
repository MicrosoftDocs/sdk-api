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

# StgSetTimes function


## -description


The <b>StgSetTimes</b> function sets the creation, access, and modification times of the indicated file, if supported by the underlying file system.


## -parameters




### -param lpszName [in]

Pointer to the name of the file to be changed.


### -param pctime [in]

Pointer to the new value for the creation time.


### -param patime [in]

Pointer to the new value for the access time.


### -param pmtime [in]

Pointer to the new value for the modification time.


## -returns



The <b>StgSetTimes</b> function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. See 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>.




## -remarks



The 
<b>StgSetTimes</b> function sets the time values for the specified file. Each of the time value parameters can be <b>NULL</b>, indicating that no modification should occur.

It is possible that one or more of these time values are not supported by the underlying file system. This function sets the times that can be set and ignores the rest.



