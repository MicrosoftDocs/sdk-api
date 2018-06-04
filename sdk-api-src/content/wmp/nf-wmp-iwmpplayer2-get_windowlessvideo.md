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

# IWMPPlayer2::get_windowlessVideo


## -description



The <b>get_windowlessVideo</b> method retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.




## -parameters




### -param pbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the Windows Media Player control renders video in windowless mode.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



By default, an embedded Windows Media Player control renders video in its own window within the client area. When the <b>VARIANT_BOOL</b> retrieved by <b>get_windowlessVideo</b> equals <b>TRUE</b>, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.

In Windows Vista, rendering video in windowless mode can degrade performance.

The <b>get_windowlessVideo</b> method is not supported for Netscape Navigator. Setting a value for this property in Navigator may yield unexpected results.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bf51d54d-d0aa-42ad-8180-d1f6487baac8">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/736eaf52-29bd-4223-a62d-d3d75cef1863">IWMPPlayer2::put_windowlessVideo</a>
 

 

