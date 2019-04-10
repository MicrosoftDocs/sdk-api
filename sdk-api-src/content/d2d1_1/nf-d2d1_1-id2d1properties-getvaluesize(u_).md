---
UID: NF:d2d1_1.ID2D1Properties.GetValueSize(U,)
title: ID2D1Properties::GetValueSize(U,) (d2d1_1.h)
author: windows-sdk-content
description: Gets the size of the property value in bytes, using the property index. This is a template overload. See Remarks.
old-location: direct2d\id2d1properties_getvaluesize2.htm
tech.root: Direct2D
ms.assetid: 98B32688-550B-4724-8715-F50C8BCD78D2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetValueSize, GetValueSize method [Direct2D], GetValueSize method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValueSize method, ID2D1Properties.GetValueSize, ID2D1Properties.GetValueSize(U,), ID2D1Properties::GetValueSize, ID2D1Properties::GetValueSize(U), ID2D1Properties::GetValueSize(U,), d2d1_1/ID2D1Properties::GetValueSize, direct2d.id2d1properties_getvaluesize2
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
 - ID2D1Properties.GetValueSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetValueSize(U,)


## -description


Gets the size of the property value in bytes, using the property index. This is a template overload. See Remarks.


## -parameters




### -param index

Type: <b>U</b>

The index of the property.


### -param arg2

TBD




## -returns



Type: <b>UINT32</b>

This method returns size of the value in bytes, using the property index
          




## -remarks



This method returns zero if <i>index</i> does not exist.




<pre class="syntax">template&lt;typename U&gt;
    UINT32 GetValueSize(
        U index
        ) CONST;
</pre>





## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

