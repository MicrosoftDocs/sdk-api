---
UID: NF:d2d1_1.ID2D1Properties.GetValueByName(PCWSTR,)
title: ID2D1Properties::GetValueByName(PCWSTR,) (d2d1_1.h)
author: windows-sdk-content
description: Gets the property value by name. This is a template overload. See Remarks.
old-location: direct2d\id2d1properties_getvaluebyname4.htm
tech.root: Direct2D
ms.assetid: 9DBC3AB6-0C58-4CC4-8851-7AF36E7FA2A7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetValueByName, GetValueByName method [Direct2D], GetValueByName method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValueByName method, ID2D1Properties.GetValueByName, ID2D1Properties.GetValueByName(PCWSTR,), ID2D1Properties::GetValueByName, ID2D1Properties::GetValueByName(PCWSTR), ID2D1Properties::GetValueByName(PCWSTR,), d2d1_1/ID2D1Properties::GetValueByName, direct2d.id2d1properties_getvaluebyname4
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
 - ID2D1Properties.GetValueByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetValueByName(PCWSTR,)


## -description


Gets the property value by name. This is a template overload. See Remarks.


## -parameters




### -param propertyName [in]

Type: <b>PCWSTR</b>

The property name to get.


### -param arg2

TBD




## -returns



Type: <b>T</b>

Returns the value requested.




## -remarks



If <i>propertyName</i> does not exist, no information is retrieved.

Any error not in the standard set returned by a property implementation will be mapped into the standard error range.


<pre class="syntax">template&lt;typename T&gt;
    T GetValueByName(
        _In_ PCWSTR propertyName
        ) const;
</pre>





## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

