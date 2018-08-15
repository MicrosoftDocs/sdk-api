---
UID: NS:ocidl.tagCADWORD
title: tagCADWORD
author: windows-sdk-content
description: Specifies a counted array of values that can be used to obtain the value corresponding to one of the predefined strings for a property.
old-location: com\cadword.htm
old-project: com
ms.assetid: 4e7f8e1a-53cc-40db-9651-00f5d912e768
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPCADWORD, CADWORD, CADWORD structure [COM], LPCADWORD, LPCADWORD structure pointer [COM], _ctrl_CADWORD, com.cadword, ocidl/CADWORD, ocidl/LPCADWORD, tagCADWORD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CADWORD, *LPCADWORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - CADWORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagCADWORD structure


## -description


Specifies a counted array of values that can be used to obtain the value corresponding to one of the predefined strings for a property.


## -struct-fields




### -field cElems

The size of the array pointed to by <b>pElems</b>.


### -field pElems

A pointer to an array of values, each of which can be passed to the <a href="https://msdn.microsoft.com/a532ebed-3ed8-4b49-a17f-f542fdbd74ff">IPerPropertyBrowsing::GetPredefinedValue</a> method to obtain the corresponding value for one of the property's predefined strings. This array is allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and is freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -see-also




<a href="https://msdn.microsoft.com/730d5e23-e84a-4629-9b59-492d8536122e">CALPOLESTR</a>



<a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">IPerPropertyBrowsing::GetPredefinedStrings</a>



<a href="https://msdn.microsoft.com/a532ebed-3ed8-4b49-a17f-f542fdbd74ff">IPerPropertyBrowsing::GetPredefinedValue</a>
 

 

