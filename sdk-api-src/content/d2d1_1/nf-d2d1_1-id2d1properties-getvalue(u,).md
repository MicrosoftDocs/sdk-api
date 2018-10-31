---
UID: NF:d2d1_1.ID2D1Properties.GetValue(U,)
title: ID2D1Properties::GetValue(U,)
author: windows-sdk-content
description: Gets the value of the property by index. This is a template overload. See Remarks.
old-location: direct2d\id2d1properties_getvalue5.htm
tech.root: direct2d
ms.assetid: 90E54C63-B584-4844-85B7-BCCF766D90E3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetValue, GetValue method [Direct2D], GetValue method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValue method, ID2D1Properties.GetValue, ID2D1Properties.GetValue(U,), ID2D1Properties::GetValue, ID2D1Properties::GetValue(U), ID2D1Properties::GetValue(U,), d2d1_1/ID2D1Properties::GetValue, direct2d.id2d1properties_getvalue5
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
 - ID2D1Properties.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetValue(U,)


## -description


Gets  the value of the property by index. This is a template overload. See Remarks.


## -parameters




### -param index

Type: <b>U</b>

The index of the property from which the value is to be obtained.


### -param arg1

TBD




## -returns



Type: <b>T</b>

Returns the value requested.




## -remarks




<pre class="syntax">template&lt;typename T, typename U&gt;
    T GetValue(
        U index
        ) const;
</pre>





## -see-also




<a href="https://msdn.microsoft.com/7261ea3c-bd52-4809-93c8-9e7a0a7424d0">D2D1_PROPERTY</a>



<a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

