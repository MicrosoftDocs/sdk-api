---
UID: NS:minidumpapiset._MINIDUMP_CALLBACK_INFORMATION
title: "_MINIDUMP_CALLBACK_INFORMATION"
author: windows-driver-content
description: Contains a pointer to an optional callback function that can be used by the MiniDumpWriteDump function.
old-location: base\minidump_callback_information_str.htm
old-project: Debug
ms.assetid: 98caf4c3-8e6b-4f42-ae48-977a8392de1c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PMINIDUMP_CALLBACK_INFORMATION, MINIDUMP_CALLBACK_INFORMATION, MINIDUMP_CALLBACK_INFORMATION structure, PMINIDUMP_CALLBACK_INFORMATION, PMINIDUMP_CALLBACK_INFORMATION structure pointer, _MINIDUMP_CALLBACK_INFORMATION, _win32_minidump_callback_information_str, base.minidump_callback_information_str, minidumpapiset/MINIDUMP_CALLBACK_INFORMATION, minidumpapiset/PMINIDUMP_CALLBACK_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MINIDUMP_CALLBACK_INFORMATION, *PMINIDUMP_CALLBACK_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_CALLBACK_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_CALLBACK_INFORMATION structure


## -description


Contains a pointer to an optional callback function that can be used by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


## -struct-fields




### -field CallbackRoutine

A pointer to the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> callback function.


### -field CallbackParam

The application-defined data for <b>CallbackRoutine</b>.


## -see-also




<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

