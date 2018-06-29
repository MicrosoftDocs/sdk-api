---
UID: NF:propapi.StgPropertyLengthAsVariant
title: StgPropertyLengthAsVariant function
author: windows-sdk-content
description: The StgPropertyLengthAsVariant function examines a SERIALIZEDPROPERTYVALUE and returns the amount of memory that this property would occupy as a PROPVARIANT.
old-location: stg\stgpropertylengthasvariant.htm
old-project: Stg
ms.assetid: 3e809ca9-3038-4d92-bb56-23bd45b6b644
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: StgPropertyLengthAsVariant, StgPropertyLengthAsVariant function [Structured Storage], propapi/StgPropertyLengthAsVariant, stg.stgpropertylengthasvariant
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - StgPropertyLengthAsVariant
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# StgPropertyLengthAsVariant function


## -description


The <b>StgPropertyLengthAsVariant</b> function examines a <b>SERIALIZEDPROPERTYVALUE</b>  and returns the amount of memory that this property would occupy as a <b>PROPVARIANT</b>.


## -parameters




### -param pProp [in]

A pointer to a <b>SERIALIZEDPROPERTYVALUE</b>.


### -param cbProp [in]

The size of the <i>pProp</i> buffer in bytes.


### -param CodePage [in]

A property set code page.


### -param bReserved [in]

Reserved. Must be 0.


## -returns



Returns the amount of memory the property would occupy as a <b>PROPVARIANT</b>.




## -remarks



Use this function to decide whether or not to deserialize a property value in a low-memory scenario.  Most applications will have no need to call this function.




## -see-also




<a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

