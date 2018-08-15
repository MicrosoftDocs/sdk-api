---
UID: NF:coml2api.StgSetTimes
title: StgSetTimes function
author: windows-sdk-content
description: The StgSetTimes function sets the creation, access, and modification times of the indicated file, if supported by the underlying file system.
old-location: stg\stgsettimes.htm
old-project: stg
ms.assetid: 5ade3e7a-a22a-458f-b463-1680893edc15
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: StgSetTimes, StgSetTimes function [Structured Storage], _stg_stgsettimes, coml2api/StgSetTimes, stg.stgsettimes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: coml2api.h
req.include-header: Objbase.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgSetTimes
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
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



