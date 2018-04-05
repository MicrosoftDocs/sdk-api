---
UID: NF:d3d9types.D3DVS_VERSION
title: D3DVS_VERSION macro
author: windows-driver-content
description: Create a vertex shader version number token.
old-location: direct3d9\d3dvs_version.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvs_version.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 9ec9757c-61df-bffc-a6d7-3132a4b25299, D3DVS_VERSION, D3DVS_VERSION macro [Direct3D 9], d3d9types/D3DVS_VERSION, direct3d9.d3dvs_version
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: d3d9types.h
req.include-header: 
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
req.typenames: D3DZBUFFERTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3d9types.h
api_name:
-	D3DVS_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DVS_VERSION macro


## -description


Create a vertex shader version number token.


## -parameters




### -param _Major

The major vertex shader version. See remarks for appropriate values.


### -param _Minor

The minor vertex shader version. See remarks for appropriate values.


## -remarks



Version Numbers

The version number is a combination of the major version and the minor vertex shader version numbers. Valid numbers are shown in the table.

<table>
<tr>
<th>Major </th>
<th>Minor</th>
<th>Example</th>
</tr>
<tr>
<td>1</td>
<td>1</td>
<td>D3DVS_VERSION(1,1)</td>
</tr>
<tr>
<td>2</td>
<td>0</td>
<td>D3DVS_VERSION(2,0)</td>
</tr>
<tr>
<td>3</td>
<td>0</td>
<td>D3DVS_VERSION(3,0)</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cabb715a-2a6a-4d56-8113-5e5ed26fc107">Macros</a>
 

 

