---
UID: NE:d2d1_1.D2D1_SUBPROPERTY
title: D2D1_SUBPROPERTY
author: windows-sdk-content
description: Specifies the indices of the system sub-properties that may be present in any property.
old-location: direct2d\__d2d1_subproperty.htm
old-project: Direct2D
ms.assetid: 311a1b6f-ef0e-4453-a5fe-d06ebb0bb222
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D2D1_SUBPROPERTY, D2D1_SUBPROPERTY enumeration [Direct2D], D2D1_SUBPROPERTY_DEFAULT, D2D1_SUBPROPERTY_DISPLAYNAME, D2D1_SUBPROPERTY_FIELDS, D2D1_SUBPROPERTY_INDEX, D2D1_SUBPROPERTY_ISREADONLY, D2D1_SUBPROPERTY_MAX, D2D1_SUBPROPERTY_MIN, d2d1_1/D2D1_SUBPROPERTY, d2d1_1/D2D1_SUBPROPERTY_DEFAULT, d2d1_1/D2D1_SUBPROPERTY_DISPLAYNAME, d2d1_1/D2D1_SUBPROPERTY_FIELDS, d2d1_1/D2D1_SUBPROPERTY_INDEX, d2d1_1/D2D1_SUBPROPERTY_ISREADONLY, d2d1_1/D2D1_SUBPROPERTY_MAX, d2d1_1/D2D1_SUBPROPERTY_MIN, direct2d.__d2d1_subproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
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
req.typenames: D2D1_SUBPROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_SUBPROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_SUBPROPERTY enumeration


## -description


Specifies the indices of the system sub-properties that may be present in any property.


## -enum-fields




### -field D2D1_SUBPROPERTY_DISPLAYNAME

The name for the parent property.


### -field D2D1_SUBPROPERTY_ISREADONLY

A Boolean indicating whether the parent property is writeable.


### -field D2D1_SUBPROPERTY_MIN

The minimum value that can be set to the parent property.


### -field D2D1_SUBPROPERTY_MAX

The maximum value that can be set to the parent property.


### -field D2D1_SUBPROPERTY_DEFAULT

The default value of the parent property.


### -field D2D1_SUBPROPERTY_FIELDS

An array of name/index pairs that indicate the possible values that can be set to the parent property.


### -field D2D1_SUBPROPERTY_INDEX

An index sub-property used by the elements of the <b>D2D1_SUBPROPERTY_FIELDS</b> array.


### -field D2D1_SUBPROPERTY_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>



<a href="https://msdn.microsoft.com/36873134-cb0e-4ba2-bddb-95b2cc92afff">ID2D1Properties::GetPropertyName</a>



<a href="https://msdn.microsoft.com/9c4b86d1-db5b-41cd-9dd4-85a8bb03dd20">ID2D1Properties::GetPropertyNameLength</a>



<a href="https://msdn.microsoft.com/6ba7ba8e-63fd-44a1-9a03-565b2e2a128c">ID2D1Properties::GetSubProperties</a>



<a href="https://msdn.microsoft.com/42e80588-9e80-4f30-9a3c-77b64f88ff7a">ID2D1Properties::GetType</a>



<a href="https://msdn.microsoft.com/01678e13-df23-47bb-9af7-9f2ecaf03577">ID2D1Properties::GetValue</a>



<a href="https://msdn.microsoft.com/fd65a610-9552-4efe-9050-715cb672acc8">ID2D1Properties::GetValueSize</a>



<a href="https://msdn.microsoft.com/7b21bcc0-b76e-4802-a8c4-ffba5ac8fa19">ID2D1Properties::SetValue</a>
 

 

