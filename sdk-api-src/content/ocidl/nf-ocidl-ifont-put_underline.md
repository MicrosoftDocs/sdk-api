---
UID: NF:ocidl.IFont.put_Underline
title: IFont::put_Underline
author: windows-sdk-content
description: Sets the font's Underline property.
old-location: com\ifont_put_underline.htm
tech.root: com
ms.assetid: c763c050-cf69-4c9d-83a9-66ccc1d4376c
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IFont interface [COM],put_Underline method, IFont.put_Underline, IFont::put_Underline, _ctrl_ifont_put_underline, com.ifont_put_underline, ocidl/IFont::put_Underline, put_Underline, put_Underline method [COM], put_Underline method [COM],IFont interface
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
 - IFont.put_Underline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::put_Underline


## -description


Sets the font's Underline property.


## -parameters




### -param underline [in]

The new Underline property for the font.
     


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
The underline state was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support an underline state. This value is not an error condition.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/714a2678-6e3d-4b8d-8632-20eb41618fff">IFont::get_Underline</a>
 

 

