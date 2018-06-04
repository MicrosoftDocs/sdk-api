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

# IDirectDrawPalette interface


## -description


Applications use the methods of the <b>IDirectDrawPalette</b> interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawPalette</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawPalette</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawPalette</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7afdea97-39b7-4dd1-8084-90ec40814735">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the palette object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae3c639f-beb4-40b6-a237-60d6e560a1c3">GetEntries</a>
</td>
<td align="left" width="63%">
Retrieves palette values from a DirectDrawPalette object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the DirectDrawPalette object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c12247b9-ecb3-4fdf-b25f-373da06df791">SetEntries</a>
</td>
<td align="left" width="63%">
Changes entries in a DirectDrawPalette object immediately.

</td>
</tr>
</table> 


## -remarks



The methods of the <b>IDirectDrawPalette</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
</tr>
<tr>
<td>Palette capabilities</td>
<td>
<a href="https://msdn.microsoft.com/7afdea97-39b7-4dd1-8084-90ec40814735">GetCaps</a>
</td>
</tr>
<tr>
<td>Palette entries</td>
<td>
<a href="https://msdn.microsoft.com/ae3c639f-beb4-40b6-a237-60d6e560a1c3">GetEntries</a> and <a href="https://msdn.microsoft.com/c12247b9-ecb3-4fdf-b25f-373da06df791">SetEntries</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWPALETTE data type to declare a variable that contains a pointer to an <b>IDirectDrawPalette</b> interface. The Ddraw.h header file declares the data type with the following code:



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirectDrawPalette    FAR *LPDIRECTDRAWPALETTE;
</pre>
</td>
</tr>
</table></span></div>


