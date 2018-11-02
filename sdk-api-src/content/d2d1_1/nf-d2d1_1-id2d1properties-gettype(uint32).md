---
UID: NF:d2d1_1.ID2D1Properties.GetType(UINT32)
title: ID2D1Properties::GetType(UINT32)
author: windows-sdk-content
description: Gets the D2D1_PROPERTY_TYPE of the selected property.
old-location: direct2d\id2d1properties_gettype.htm
tech.root: direct2d
ms.assetid: 42e80588-9e80-4f30-9a3c-77b64f88ff7a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetType, GetType method [Direct2D], GetType method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetType method, ID2D1Properties.GetType, ID2D1Properties.GetType(UINT32), ID2D1Properties::GetType, ID2D1Properties::GetType(UINT32), d2d1_1/ID2D1Properties::GetType, direct2d.id2d1properties_gettype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetType(UINT32)


## -description


Gets the <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a> of the selected property.




## -parameters




### -param index

Type: <b>UINT32</b>

The index of the property for which the type will be retrieved.


## -returns



Type: <b><a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a></b>

This method returns a <a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a>-typed value for the type of the selected property.




## -remarks



If the property does not exist, the method returns <a href="__d2d1_property_type.htm">D2D1_PROPERTY_TYPE_UNKNOWN</a>.




## -see-also




<a href="https://msdn.microsoft.com/7261ea3c-bd52-4809-93c8-9e7a0a7424d0">D2D1_PROPERTY</a>



<a href="https://msdn.microsoft.com/6535d71a-c76c-462c-9972-4db7e4ef383d">D2D1_PROPERTY_TYPE</a>



<a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

