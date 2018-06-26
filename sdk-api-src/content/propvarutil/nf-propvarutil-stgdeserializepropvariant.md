---
UID: NF:propvarutil.StgDeserializePropVariant
title: StgDeserializePropVariant function
author: windows-sdk-content
description: The StgDeserializePropVariant function converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.
old-location: stg\stgdeserializepropvariant.htm
old-project: Stg
ms.assetid: 55b4de40-d81d-4989-8f57-a286815fa495
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: StgDeserializePropVariant, StgDeserializePropVariant function [Structured Storage], propvarutil/StgDeserializePropVariant, stg.stgdeserializepropvariant
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - StgDeserializePropVariant
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll
req.irql: 
req.product: ADAM
---

# StgDeserializePropVariant function


## -description


The <b>StgDeserializePropVariant</b> function converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.


## -parameters




### -param pprop [in]

A pointer to the  <b>SERIALIZEDPROPERTYVALUE</b> buffer.


### -param cbMax [in]

The size of the <i>pprop</i> buffer in bytes.


### -param ppropvar

TBD




#### - pvar [out]

A pointer to a <b>PROPVARIANT</b>.


## -returns



This function can return one of these values.




## -remarks



This function deserializes a <b>PROPVARIANT</b> data type. This function is similar to the <a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a> function. The <b>StgDeserializePropVariant</b> function uses the default value of <b>CP_WINUNICODE</b> for the code page and a system provided allocator that uses task memory.  Use <b>StgDeserializePropVariant</b> unless you want to specify which code page and memory allocator to use.




## -see-also




<a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a>



<a href="https://msdn.microsoft.com/e1382c1e-3f9e-41a2-8e95-fc3702e516d3">StgSerializePropVariant</a>
 

 

