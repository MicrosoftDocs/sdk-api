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

# MINIDUMP_CALLBACK_ROUTINE callback function


## -description


An application-defined callback function used with 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>. It receives extended minidump information.

The <b>MINIDUMP_CALLBACK_ROUTINE</b> type defines a pointer to this callback function. 
<b>MiniDumpCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param CallbackParam [in]

An application-defined parameter value.


### -param CallbackInput [in]

A pointer to a 
<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a> structure that specifies extended minidump information.


### -param CallbackOutput [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/57949087-0f22-40c8-ab56-326a8304c310">MINIDUMP_CALLBACK_OUTPUT</a> structure that receives application-defined information from the callback function.


## -returns



If the function succeeds, return <b>TRUE</b>; otherwise, return <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/98caf4c3-8e6b-4f42-ae48-977a8392de1c">MINIDUMP_CALLBACK_INFORMATION</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

