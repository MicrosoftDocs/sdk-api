---
UID: NS:ocidl.tagCALPOLESTR
title: tagCALPOLESTR
author: windows-sdk-content
description: Specifies a counted array of strings used to specify the predefined strings that a property can accept.
old-location: com\calpolestr.htm
tech.root: com
ms.assetid: 730d5e23-e84a-4629-9b59-492d8536122e
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPCALPOLESTR, CALPOLESTR, CALPOLESTR structure [COM], LPCALPOLESTR, LPCALPOLESTR structure pointer [COM], _ctrl_CALPOLESTR, com.calpolestr, ocidl/CALPOLESTR, ocidl/LPCALPOLESTR, tagCALPOLESTR"
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
 - CALPOLESTR
product: Windows
targetos: Windows
req.typenames: CALPOLESTR, *LPCALPOLESTR
req.redist: 
---

# tagCALPOLESTR structure


## -description


Specifies a counted array of strings used to specify the predefined strings that a property can accept.


## -struct-fields




### -field cElems

The size of the array pointed to by <b>pElems</b>.


### -field pElems

A pointer to an array of <a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">LPOLESTR</a> values, each of which corresponds to an allowable value that a particular property can accept. The caller can use these string values in user interface elements, such as drop-down list boxes. This array, as well as the strings in the array, are allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and is freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -see-also




<a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">IPerPropertyBrowsing::GetPredefinedStrings</a>



<a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">LPOLESTR</a>
 

 

