---
UID: NF:propidl.StgConvertPropertyToVariant
title: StgConvertPropertyToVariant function
author: windows-sdk-content
description: Converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.
old-location: stg\stgconvertpropertytovariant.htm
tech.root: Stg
ms.assetid: ea4196e6-fc99-4288-942a-e5283f2e5544
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StgConvertPropertyToVariant, StgConvertPropertyToVariant function [Structured Storage], propidl/StgConvertPropertyToVariant, stg.stgconvertpropertytovariant
ms.topic: function
req.header: propidl.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - StgConvertPropertyToVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StgConvertPropertyToVariant function


## -description


The <b>StgConvertPropertyToVariant</b> function converts a <b>SERIALIZEDPROPERTYVALUE</b> data type to a <b>PROPVARIANT</b> data type.


## -parameters




### -param pprop [in]

A pointer to <b>SERIALIZEDPROPERTYVALUE</b>.


### -param CodePage [in]

A property set codepage.


### -param pvar [out]

A pointer to <b>PROPVARIANT</b>.


### -param pma [in]

A pointer to a class that implements the <a href="https://msdn.microsoft.com/a0735b62-5ed3-42df-a320-b58c742645a8">IMemoryAllocator</a> abstract class.


## -returns



Returns <b>TRUE</b> is the property converted was an indirect type (<b>VT_STREAM</b> or <b>VT_STREAMED_OBJECT</b>); otherwise <b>FALSE</b>.




## -remarks



This function converts a property  to a <b>PROPVARIANT</b> data type. If the function fails, it throws an exception that represents an <b>NT_STATUS</b> such as <b>STATUS_INVALID_PARAMETER</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

