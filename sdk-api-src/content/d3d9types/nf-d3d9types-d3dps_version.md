---
UID: NF:d3d9types.D3DPS_VERSION
title: D3DPS_VERSION macro
author: windows-driver-content
description: Create a pixel shader version token.
old-location: direct3d9\d3dps_version.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dps_version.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 42f6aa87-db2f-0c03-5116-fd3fd9234d71, D3DPS_VERSION, D3DPS_VERSION macro [Direct3D 9], d3d9types/D3DPS_VERSION, direct3d9.d3dps_version
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
-	D3DPS_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DPS_VERSION macro


## -description


Create a pixel shader version token.


## -parameters




### -param _Major

The major pixel shader version.


### -param _Minor

The minor pixel shader version.


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
<td>D3DPS_VERSION(1,1)</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
<td>D3DPS_VERSION(1,2)</td>
</tr>
<tr>
<td>1</td>
<td>3</td>
<td>D3DPS_VERSION(1,3)</td>
</tr>
<tr>
<td>1</td>
<td>4</td>
<td>D3DPS_VERSION(1,4)</td>
</tr>
<tr>
<td>2</td>
<td>0</td>
<td>D3DPS_VERSION(2,0)</td>
</tr>
<tr>
<td>3</td>
<td>0</td>
<td>D3DPS_VERSION(3,0)</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/cabb715a-2a6a-4d56-8113-5e5ed26fc107">Macros</a>
 

 

