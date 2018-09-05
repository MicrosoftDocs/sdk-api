---
UID: NF:httpserv.IHttpPerfCounterInfo.DecrementCounter
title: DecrementCounter function
author: windows-sdk-content
description: Decrements the object's hidden counter.
old-location: direct3dhlsl\sm5_object_rwstructuredbuffer_decrementcounter.htm
old-project: direct3dhlsl
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: 124c9e6b-c1d0-9cae-e977-58ca435d9cb9, DecrementCounter, DecrementCounter function [HLSL], RWStructuredBuffer, direct3dhlsl.sm5_object_rwstructuredbuffer_decrementcounter, httpserv/DecrementCounter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: httpserv.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: HTTP_VERSION, *PHTTP_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - httpserv.h
api_name:
 - DecrementCounter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DecrementCounter function


## -description


Decrements the object's hidden counter.


## -parameters




### -param dwCounterIndex

TBD


### -param dwValue

TBD




## -returns



Type: <b>uint</b>

The post-decremented counter value.




## -remarks



The bound unordered access view must have <a href="https://msdn.microsoft.com/13cf0083-c61a-478d-94bd-00dec4cf27b7">D3D11_BUFFER_UAV_FLAG_COUNTER</a> set during creationfor this method to work.

This function is supported for the following types of shaders:

<table>
<tr>
<th>Vertex</th>
<th>Hull</th>
<th>Domain</th>
<th>Geometry</th>
<th>Pixel</th>
<th>Compute</th>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td>x</td>
<td>x</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8dd93b81-135d-4f28-898f-38510dc39af1">RWStructuredBuffer</a>



<a href="https://msdn.microsoft.com/ec646940-8901-45c5-a44c-434c8acae2aa">Shader Model 5</a>
 

 

