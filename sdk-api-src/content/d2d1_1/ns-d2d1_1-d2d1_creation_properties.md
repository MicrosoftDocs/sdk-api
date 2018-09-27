---
UID: NS:d2d1_1.D2D1_CREATION_PROPERTIES
title: D2D1_CREATION_PROPERTIES
author: windows-sdk-content
description: Specifies the options with which the Direct2D device, factory, and device context are created.
old-location: direct2d\d2d1_creation_properties.htm
tech.root: direct2d
ms.assetid: 657439fe-dc17-42af-9e2c-2f3cb769a5a3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D2D1_CREATION_PROPERTIES, D2D1_CREATION_PROPERTIES structure [Direct2D], PD2D1_CREATION_PROPERTIES, PD2D1_CREATION_PROPERTIES structure pointer [Direct2D], d2d1_1/D2D1_CREATION_PROPERTIES, d2d1_1/PD2D1_CREATION_PROPERTIES, direct2d.d2d1_creation_properties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_CREATION_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_CREATION_PROPERTIES
req.redist: 
---

# D2D1_CREATION_PROPERTIES structure


## -description


Specifies the options with which the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device, factory, and device context are created.



## -struct-fields




### -field threadingMode

The threading mode with which the corresponding root objects will be created.


### -field debugLevel

The debug level that the root objects should be created with.


### -field options

The device context options that the root objects should be created with.


## -remarks



The root objects referred to here are the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device, Direct2D factory and the Direct2D device context.





## -see-also




<a href="https://msdn.microsoft.com/5ed3ec21-b609-41b6-9568-6ede460bc395">D2D1CreateDevice</a>



<a href="https://msdn.microsoft.com/0e56d057-20a5-47b7-aec9-63c8e31f349b">D2D1CreateDeviceContext</a>
 

 

