---
UID: NF:propvarutil.StgSerializePropVariant
title: StgSerializePropVariant function
author: windows-sdk-content
description: The StgSerializePropVariant function converts a PROPVARIANT data type to a SERIALIZEDPROPERTYVALUE data type.
old-location: stg\StgSerializePropVariant.htm
tech.root: Stg
ms.assetid: e1382c1e-3f9e-41a2-8e95-fc3702e516d3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: StgSerializePropVariant, StgSerializePropVariant function [Structured Storage], propvarutil/StgSerializePropVariant, stg.StgSerializePropVariant
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Propsys.lib
req.dll: Propsys.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - StgSerializePropVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StgSerializePropVariant function


## -description


The <b>StgSerializePropVariant</b> function converts a <b>PROPVARIANT</b> data type to a <b>SERIALIZEDPROPERTYVALUE</b> data type.


## -parameters




### -param ppropvar [in]

A pointer to <b>PROPVARIANT</b>.


### -param ppProp [out]

A pointer to the newly allocated  <b>SERIALIZEDPROPERTYVALUE</b>.


### -param pcb [out]

A pointer to the size of the newly allocated  <b>SERIALIZEDPROPERTYVALUE</b>.


## -returns



This function can return one of these values.




## -remarks



The 
 <b>StgSerializePropVariant</b> function serializes a <b>PROPVARIANT</b>.  The function is similar to the <a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a> function, but   the <b>StgSerializePropVariant</b> function automatically handles memory allocation for the new <b>SERIALIZEDPROPERTYVALUE</b>.  In addition, <b>StgSerializePropVariant</b> uses the default values <b>CP_WINUNICODE</b> and PID_ILLEGAL for code page and property ID respectively.  Use <b>StgSerializePropVariant</b> unless control over these arguments is specifically needed.




## -see-also




<a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

