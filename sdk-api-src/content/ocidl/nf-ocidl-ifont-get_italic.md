---
UID: NF:ocidl.IFont.get_Italic
title: IFont::get_Italic
author: windows-sdk-content
description: Gets the font's current Italic property.
old-location: com\ifont_get_italic.htm
tech.root: com
ms.assetid: d56c21d6-1296-4c0c-a13e-8e4b3164e747
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFont interface [COM],get_Italic method, IFont.get_Italic, IFont::get_Italic, _ctrl_ifont_get_italic, com.ifont_get_italic, get_Italic, get_Italic method [COM], get_Italic method [COM],IFont interface, ocidl/IFont::get_Italic
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
 - IFont.get_Italic
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::get_Italic


## -description


Gets the font's current Italic property.


## -parameters




### -param pItalic [out]

A pointer to the caller-allocated variable that receives the current Italic property for the font.


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
        *<i>pItalic</i> to <b>FALSE</b> and return 
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
The address in pitalic is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/a59169e1-d3c4-4dc0-b228-afad0e4d4307">IFont::put_Italic</a>
 

 

