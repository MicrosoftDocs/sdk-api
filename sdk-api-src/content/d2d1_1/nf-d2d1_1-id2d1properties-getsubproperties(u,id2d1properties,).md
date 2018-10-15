---
UID: NF:d2d1_1.ID2D1Properties.GetSubProperties(U,ID2D1Properties,)
title: ID2D1Properties::GetSubProperties(U,ID2D1Properties,)
author: windows-sdk-content
description: Gets the sub-properties of the provided property by index. This is a template overload.
old-location: direct2d\id2d1properties_getsubproperties2.htm
tech.root: direct2d
ms.assetid: D7A79C72-6BFC-4603-82AD-FFEEA91B6CBE
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetSubProperties, GetSubProperties method [Direct2D], GetSubProperties method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetSubProperties method, ID2D1Properties.GetSubProperties, ID2D1Properties.GetSubProperties(U,ID2D1Properties,), ID2D1Properties::GetSubProperties, ID2D1Properties::GetSubProperties(U,ID2D1Properties**), ID2D1Properties::GetSubProperties(U,ID2D1Properties,), d2d1_1/ID2D1Properties::GetSubProperties, direct2d.id2d1properties_getsubproperties2
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
 - ID2D1Properties.GetSubProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetSubProperties(U,ID2D1Properties,)


## -description


Gets the sub-properties of the provided property by index. This is a template overload. See Remarks.


## -parameters




### -param index

Type: <b>U</b>

The index of the  sub-properties to be retrieved.


### -param subProperties [out]

Type: <b><a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>**</b>

When this method returns, contains the address of a pointer to the sub-properties.


### -param arg1

TBD




## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_NO_SUBPROPERTIES</td>
<td>The specified property does not exist.</td>
</tr>
</table>
 




## -remarks



If there are no sub-properties, <i>subProperties</i> will be <b>NULL</b>, and <b>D2DERR_NO_SUBPROPERTIES</b> will be returned.
      


<pre class="syntax">template&lt;typename U&gt;
          HRESULT GetSubProperties(
          U index,
          _Outptr_opt_ ID2D1Properties **subProperties
          ) CONST;
        </pre>





## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

