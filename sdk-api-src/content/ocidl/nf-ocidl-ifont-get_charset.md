---
UID: NF:ocidl.IFont.get_Charset
title: IFont::get_Charset
author: windows-sdk-content
description: Retrieves the character set used in the font.
old-location: com\ifont_get_charset.htm
tech.root: com
ms.assetid: 3a784453-db29-4917-90ee-8893f787646a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFont interface [COM],get_Charset method, IFont.get_Charset, IFont::get_Charset, _ctrl_ifont_get_charset, com.ifont_get_charset, get_Charset, get_Charset method [COM], get_Charset method [COM],IFont interface, ocidl/IFont::get_Charset
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
 - IFont.get_Charset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::get_Charset


## -description


Retrieves the character set used in the font. The character set can be any of those defined 
   for Windows fonts.


## -parameters




### -param pCharset [out]

A pointer to the caller-allocated variable that receives the character set 
      value.


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
The character set was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pCharset</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/da48fefa-28d2-41aa-a324-dc259504c9ed">IFont::put_Charset</a>
 

 

