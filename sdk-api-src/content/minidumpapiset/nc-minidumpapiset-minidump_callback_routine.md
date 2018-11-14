---
UID: NC:minidumpapiset.MINIDUMP_CALLBACK_ROUTINE
title: MINIDUMP_CALLBACK_ROUTINE
author: windows-sdk-content
description: An application-defined callback function used with MiniDumpWriteDump. It receives extended minidump information.
old-location: base\minidumpcallback.htm
tech.root: debug
ms.assetid: 8dc95b0a-6aee-4c38-ab25-a800153bbe91
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: MINIDUMP_CALLBACK_ROUTINE, MiniDumpCallback, MiniDumpCallback callback, MiniDumpCallback callback function, _win32_minidumpcallback, base.minidumpcallback, minidumpapiset/MiniDumpCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
 - minidumpapiset.h
api_name:
 - MiniDumpCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
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
 

 

