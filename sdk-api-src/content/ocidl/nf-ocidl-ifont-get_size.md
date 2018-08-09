---
UID: NF:ocidl.IFont.get_Size
title: IFont::get_Size
author: windows-sdk-content
description: Retrieves the point size of the font.
old-location: com\ifont_get_size.htm
old-project: com
ms.assetid: aeee7dfc-5ccd-4c30-a59e-5eec93505288
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFont interface [COM],get_Size method, IFont.get_Size, IFont::get_Size, _ctrl_ifont_get_size, com.ifont_get_size, get_Size, get_Size method [COM], get_Size method [COM],IFont interface, ocidl/IFont::get_Size
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.get_Size
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IFont::get_Size


## -description


Retrieves the point size of the font.


## -parameters




### -param pSize [out]

 A pointer to the caller-allocated variable that receives the size,  in <b>HIMETRIC</b> 
   units.


## -returns



The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the 
      following values.

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
The size was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pSize</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">IFont::put_Size</a>
 

 

