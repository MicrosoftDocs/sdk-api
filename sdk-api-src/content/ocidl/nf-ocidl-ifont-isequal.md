---
UID: NF:ocidl.IFont.IsEqual
title: IFont::IsEqual
author: windows-sdk-content
description: Compares this font object to another for equivalence.
old-location: com\ifont_isequal.htm
tech.root: com
ms.assetid: becef75d-8342-4b4f-82e2-f1cca4eb619e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IFont interface [COM],IsEqual method, IFont.IsEqual, IFont::IsEqual, IsEqual, IsEqual method [COM], IsEqual method [COM],IFont interface, _ctrl_ifont_isequal, com.ifont_isequal, ocidl/IFont::IsEqual
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
 - IFont.IsEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::IsEqual


## -description


Compares this font object to another for equivalence.


## -parameters




### -param pFontOther [in]

A pointer to the <a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a> interface on the font object to be compared to this font. The reference count of the object referred to by this pointer is not affected by the comparison operation.
     


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
The two fonts are equivalent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The two fonts are not equivalent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pFontOther</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>
 

 

