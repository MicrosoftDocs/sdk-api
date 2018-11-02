---
UID: NS:d2d1effectauthor.D2D1_PROPERTY_BINDING
title: D2D1_PROPERTY_BINDING
author: windows-sdk-content
description: Defines a property binding to a pair of functions which get and set the corresponding property.
old-location: direct2d\d2d1_property_binding.htm
tech.root: direct2d
ms.assetid: 0eb6d428-cb65-4738-9cf3-64038b728004
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_PROPERTY_BINDING, D2D1_PROPERTY_BINDING structure [Direct2D], d2d1effectauthor/D2D1_PROPERTY_BINDING, direct2d.d2d1_property_binding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1effectauthor.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effectauthor.h
api_name:
 - D2D1_PROPERTY_BINDING
product: Windows
targetos: Windows
req.typenames: D2D1_PROPERTY_BINDING
req.redist: 
---

# D2D1_PROPERTY_BINDING structure


## -description


Defines a property binding to a pair of functions which get and set the corresponding property. 


## -struct-fields




### -field propertyName

 The name of the property.


### -field setFunction

 The function that will receive the data to set.


### -field getFunction

The function that will be asked to write the output data.


## -remarks



The <b>propertyName</b> is used to cross-correlate the property binding with the registration XML. The <b>propertyName</b> must be present in the XML call or the registration will fail.



All properties must be bound.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory::RegisterEffect</a>
 

 

