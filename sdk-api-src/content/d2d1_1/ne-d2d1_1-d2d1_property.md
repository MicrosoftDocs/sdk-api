---
UID: NE:d2d1_1.D2D1_PROPERTY
title: D2D1_PROPERTY
author: windows-sdk-content
description: Specifies the indices of the system properties present on the ID2D1Properties interface for an ID2D1Effect.
old-location: direct2d\__d2d1_property.htm
old-project: direct2d
ms.assetid: 7261ea3c-bd52-4809-93c8-9e7a0a7424d0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_PROPERTY, D2D1_PROPERTY , D2D1_PROPERTY enumeration [Direct2D], D2D1_PROPERTY_AUTHOR, D2D1_PROPERTY_CACHED, D2D1_PROPERTY_CATEGORY, D2D1_PROPERTY_CLSID, D2D1_PROPERTY_DESCRIPTION, D2D1_PROPERTY_DISPLAYNAME, D2D1_PROPERTY_INPUTS, D2D1_PROPERTY_MAX_INPUTS, D2D1_PROPERTY_MIN_INPUTS, D2D1_PROPERTY_PRECISION, d2d1_1/D2D1_PROPERTY, d2d1_1/D2D1_PROPERTY_AUTHOR, d2d1_1/D2D1_PROPERTY_CACHED, d2d1_1/D2D1_PROPERTY_CATEGORY, d2d1_1/D2D1_PROPERTY_CLSID, d2d1_1/D2D1_PROPERTY_DESCRIPTION, d2d1_1/D2D1_PROPERTY_DISPLAYNAME, d2d1_1/D2D1_PROPERTY_INPUTS, d2d1_1/D2D1_PROPERTY_MAX_INPUTS, d2d1_1/D2D1_PROPERTY_MIN_INPUTS, d2d1_1/D2D1_PROPERTY_PRECISION, direct2d.__d2d1_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_PROPERTY enumeration


## -description


Specifies the indices of the system properties present on the <a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a> interface for an <a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>.


## -enum-fields




### -field D2D1_PROPERTY_CLSID

The CLSID of the effect.


### -field D2D1_PROPERTY_DISPLAYNAME

The name of the effect.


### -field D2D1_PROPERTY_AUTHOR

The author of the effect.


### -field D2D1_PROPERTY_CATEGORY

The category of the effect.


### -field D2D1_PROPERTY_DESCRIPTION

The description of the effect.


### -field D2D1_PROPERTY_INPUTS

The names of the effect's inputs.


### -field D2D1_PROPERTY_CACHED

The output of the effect should be cached. 


### -field D2D1_PROPERTY_PRECISION

The buffer precision of the effect output.


### -field D2D1_PROPERTY_MIN_INPUTS

The minimum number of inputs supported by the effect.


### -field D2D1_PROPERTY_MAX_INPUTS

The maximum number of inputs supported by the effect.


### -field D2D1_PROPERTY_FORCE_DWORD




## -remarks



Under normal circumstances the minimum and maximum number of inputs to the effect are the same. If the effect supports a variable number of inputs, the <a href="https://msdn.microsoft.com/cdcaa997-acbe-40e3-9439-629b3853d8d4">ID2D1Effect::SetNumberOfInputs</a> method can be used to choose the number that the application will enable.




## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>



<a href="https://msdn.microsoft.com/36873134-cb0e-4ba2-bddb-95b2cc92afff">ID2D1Properties::GetPropertyName</a>



<a href="https://msdn.microsoft.com/9c4b86d1-db5b-41cd-9dd4-85a8bb03dd20">ID2D1Properties::GetPropertyNameLength</a>



<a href="https://msdn.microsoft.com/6ba7ba8e-63fd-44a1-9a03-565b2e2a128c">ID2D1Properties::GetSubProperties</a>



<a href="https://msdn.microsoft.com/42e80588-9e80-4f30-9a3c-77b64f88ff7a">ID2D1Properties::GetType</a>



<a href="https://msdn.microsoft.com/01678e13-df23-47bb-9af7-9f2ecaf03577">ID2D1Properties::GetValue</a>



<a href="https://msdn.microsoft.com/fd65a610-9552-4efe-9050-715cb672acc8">ID2D1Properties::GetValueSize</a>



<a href="https://msdn.microsoft.com/7b21bcc0-b76e-4802-a8c4-ffba5ac8fa19">ID2D1Properties::SetValue</a>
 

 

