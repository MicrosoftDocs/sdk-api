---
UID: NS:ocidl.tagCAUUID
title: tagCAUUID
author: windows-sdk-content
description: Specifies a counted array of UUID or GUID types used to receive an array of CLSIDs for the property pages that the object wants to display.
old-location: com\cauuid.htm
tech.root: com
ms.assetid: 23b991fb-9494-4d3b-83df-986739beaa14
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: "*LPCAUUID, CAUUID, CAUUID structure [COM], LPCAUUID, LPCAUUID structure pointer [COM], _ctrl_CAUUID, com.cauuid, ocidl/CAUUID, ocidl/LPCAUUID, tagCAUUID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OCIdl.h
api_name:
 - CAUUID
product: Windows
targetos: Windows
req.typenames: CAUUID, *LPCAUUID
req.redist: 
---

# tagCAUUID structure


## -description


Specifies a counted array of UUID or GUID types used to receive an array of CLSIDs for the property pages that the object wants to display.


## -struct-fields




### -field cElems

The size of the array pointed to by <b>pElems</b>.


### -field pElems

A pointer to an array of values, each of which specifies a CLSID of a particular property page. This array is allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and is freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -see-also




<a href="https://msdn.microsoft.com/82b652da-b49a-47a7-a959-522b051bfd59">ISpecifyPropertyPages::GetPages</a>
 

 

