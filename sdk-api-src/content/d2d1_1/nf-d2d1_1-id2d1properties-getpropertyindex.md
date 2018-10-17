---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyIndex
title: ID2D1Properties::GetPropertyIndex
author: windows-sdk-content
description: Gets the index corresponding to the given property name.
old-location: direct2d\id2d1properties_getpropertyindex.htm
tech.root: direct2d
ms.assetid: b1c7003f-b7c2-464c-8e8e-a641068b9393
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetPropertyIndex, GetPropertyIndex method [Direct2D], GetPropertyIndex method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyIndex method, ID2D1Properties.GetPropertyIndex, ID2D1Properties::GetPropertyIndex, d2d1_1/ID2D1Properties::GetPropertyIndex, direct2d.id2d1properties_getpropertyindex
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
req.lib: 
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
 - ID2D1Properties.GetPropertyIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetPropertyIndex


## -description


Gets the index corresponding to the given property name. 


## -parameters




### -param name [in]

Type: <b>PCWSTR</b>

The name of the property to retrieve.


## -returns



Type: <b>UINT32</b>

The index of the corresponding property name.




## -remarks



 If the property does not exist, this method returns <a href="https://msdn.microsoft.com/912207f4-90fc-47f6-851a-6537cfe80d49">D2D1_INVALID_PROPERTY_INDEX</a>. This reserved value will never map to a valid index and will cause <b>NULL</b> or sentinel values to be returned from other parts of the property interface.




## -see-also




<a href="https://msdn.microsoft.com/912207f4-90fc-47f6-851a-6537cfe80d49">D2D1_INVALID_PROPERTY_INDEX</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

