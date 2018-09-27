---
UID: NF:ocidl.IFont.get_Strikethrough
title: IFont::get_Strikethrough
author: windows-sdk-content
description: Gets the font's current Strikethrough property.
old-location: com\ifont_get_strikethrough.htm
tech.root: com
ms.assetid: e70ea85a-fc76-412c-a100-c834dc8f0208
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFont interface [COM],get_Strikethrough method, IFont.get_Strikethrough, IFont::get_Strikethrough, _ctrl_ifont_get_strikethrough, com.ifont_get_strikethrough, get_Strikethrough, get_Strikethrough method [COM], get_Strikethrough method [COM],IFont interface, ocidl/IFont::get_Strikethrough
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.get_Strikethrough
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::get_Strikethrough


## -description


Gets the font's current  Strikethrough property.


## -parameters




### -param pStrikethrough [out]

A pointer to the caller-allocated variable that receives the current Strikethrough property for the font.


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
The state was retrieved successfully. If the state is indeterminate, a font object should set 
        *<i>pStrikethrough</i> to <b>FALSE</b> and return 
        <b>S_OK</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pStrikethrough</i> parameter is not valid. For example, it may 
        be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/32b9c3aa-4c89-441e-9b41-0ac6d8a52bba">IFont::put_Strikethrough</a>
 

 

