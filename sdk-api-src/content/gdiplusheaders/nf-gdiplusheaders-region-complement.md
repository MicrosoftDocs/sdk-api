---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Region::Complement


## -description


<span>This topic lists the 
			Complement methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a> class. For a complete list of methods for the <b>Region</b> class, see <a href="https://msdn.microsoft.com/bbaa4027-94aa-497f-8efb-a82d251847af">Region Methods</a>.

</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a83d400f-0a3d-4486-a9a7-831455908ff8">Complement(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a83d400f-0a3d-4486-a9a7-831455908ff8">Region::Complement</a> method updates this region to the portion of the specified rectangle's interior that does not intersect this region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40ddcb50-60f7-48b6-a0cb-b0c946f9acf2">Complement(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/40ddcb50-60f7-48b6-a0cb-b0c946f9acf2">Region::Complement</a> method updates this region to the portion of the specified rectangle's interior that does not intersect this region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/084846dd-1459-40f4-9db2-db8995d37bd7">Complement(Region*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/084846dd-1459-40f4-9db2-db8995d37bd7">Region::Complement</a> method updates this region to the portion of another region that does not intersect this region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003454a9-5439-463c-939d-a48555ac91b6">Complement(GraphicsPath*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/003454a9-5439-463c-939d-a48555ac91b6">Region::Complement</a> method updates this region to the portion of the specified path's interior that does not intersect this region.

</td>
</tr>
</table>

## -parameters

