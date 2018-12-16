---
UID: NS:minidumpapiset._MINIDUMP_STRING
title: MINIDUMP_STRING
author: windows-sdk-content
description: Describes a string.
old-location: base\minidump_string_str.htm
tech.root: debug
ms.assetid: b90b2b29-9d39-4a73-b5fb-bb6e04c94811
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_STRING, MINIDUMP_STRING, MINIDUMP_STRING structure, PMINIDUMP_STRING, PMINIDUMP_STRING structure pointer, _MINIDUMP_STRING, _win32_minidump_string_str, base.minidump_string_str, minidumpapiset/MINIDUMP_STRING, minidumpapiset/PMINIDUMP_STRING"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_STRING
product: Windows
targetos: Windows
req.typenames: MINIDUMP_STRING, *PMINIDUMP_STRING
req.redist: DbgHelp.dll 5.1 or later
---

# MINIDUMP_STRING structure


## -description


Describes a string.


## -struct-fields




### -field Length

The size of the string in the <b>Buffer</b> member, in bytes. This size does not include the null-terminating character.


### -field Buffer

The null-terminated string.


## -see-also




<a href="https://msdn.microsoft.com/8387513a-137a-418e-8341-8066965849e6">MINIDUMP_HANDLE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/17e32c6e-29df-4308-b22d-39e13bc6a2a5">MINIDUMP_MODULE</a>



<a href="https://msdn.microsoft.com/d2ae58fa-561c-4135-a757-88598ebda57a">MINIDUMP_UNLOADED_MODULE</a>
 

 

