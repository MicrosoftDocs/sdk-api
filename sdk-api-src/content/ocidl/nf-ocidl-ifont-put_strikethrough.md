---
UID: NF:ocidl.IFont.put_Strikethrough
title: IFont::put_Strikethrough method
author: windows-driver-content
description: Sets the font's Strikethrough property.
old-location: com\ifont_put_strikethrough.htm
old-project: com
ms.assetid: 32b9c3aa-4c89-441e-9b41-0ac6d8a52bba
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IFont, IFont interface [COM], put_Strikethrough method, IFont::put_Strikethrough, _ctrl_ifont_put_strikethrough, com.ifont_put_strikethrough, ocidl/IFont::put_Strikethrough, put_Strikethrough method [COM], put_Strikethrough method [COM], IFont interface, put_Strikethrough,IFont.put_Strikethrough
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IFont.put_Strikethrough
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IFont::put_Strikethrough method


## -description


Sets the font's Strikethrough property.


## -parameters




### -param strikethrough [in]

The new Strikethrough property for the font.


## -returns



This method can return one of these values.

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
The Strikethrough property was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support a strikethrough state. This value is not an error condition.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/e70ea85a-fc76-412c-a100-c834dc8f0208">IFont::get_Strikethrough</a>
 

 

