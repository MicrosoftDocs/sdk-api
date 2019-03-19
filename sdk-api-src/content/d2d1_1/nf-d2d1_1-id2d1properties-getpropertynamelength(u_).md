---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyNameLength(U,)
title: ID2D1Properties::GetPropertyNameLength(U,) (d2d1_1.h)
author: windows-sdk-content
description: Gets the number of characters for the given property name. This is a template overload. See Remarks.
old-location: direct2d\id2d1properties_getpropertynamelength2.htm
tech.root: Direct2D
ms.assetid: 245A71F7-4034-4D65-A9EB-9A33FC8DED05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPropertyNameLength, GetPropertyNameLength method [Direct2D], GetPropertyNameLength method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyNameLength method, ID2D1Properties.GetPropertyNameLength, ID2D1Properties.GetPropertyNameLength(U,), ID2D1Properties::GetPropertyNameLength, ID2D1Properties::GetPropertyNameLength(U), ID2D1Properties::GetPropertyNameLength(U,), d2d1_1/ID2D1Properties::GetPropertyNameLength, direct2d.id2d1properties_getpropertynamelength2
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
 - ID2D1Properties.GetPropertyNameLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetPropertyNameLength(U,)


## -description


Gets  the number of characters for the given property name.  This is a template overload. See Remarks.


## -parameters




### -param index

Type: <b>U</b>

The index of the property name to retrieve.


### -param arg2

TBD




## -returns



Type: <b>UINT32</b>

This method returns the size in characters of the name corresponding to the given property index, or zero if the property index does not exist. 




## -remarks



The value returned by this method can be used to ensure that the buffer size for <a href="https://msdn.microsoft.com/36873134-cb0e-4ba2-bddb-95b2cc92afff">GetPropertyName</a> is appropriate. 


<pre class="syntax">template&lt;typename U&gt;
    UINT32 GetPropertyNameLength(
        U index
        ) CONST;
</pre>





## -see-also




<a href="https://msdn.microsoft.com/7261ea3c-bd52-4809-93c8-9e7a0a7424d0">D2D1_PROPERTY</a>



<a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

