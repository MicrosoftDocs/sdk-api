---
UID: NF:msinkaut.IInkLineInfo.GetFormat
title: IInkLineInfo::GetFormat
author: windows-sdk-content
description: Returns the display properties currently set on the text ink object (tInk).
old-location: tablet\iinklineinfo_getformat.htm
tech.root: tablet
ms.assetid: 8f894963-7075-46f4-8809-82d1aa7e13e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 8f894963-7075-46f4-8809-82d1aa7e13e7, GetFormat, GetFormat method [Tablet PC], GetFormat method [Tablet PC],IInkLineInfo interface, IInkLineInfo interface [Tablet PC],GetFormat method, IInkLineInfo.GetFormat, IInkLineInfo::GetFormat, msinkaut/IInkLineInfo::GetFormat, tablet.iinklineinfo_getformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkLineInfo.GetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkLineInfo::GetFormat


## -description



Returns the display properties currently set on the text ink object (tInk).




## -parameters




### -param pim [out]

A pointer to an <a href="https://msdn.microsoft.com/27d56034-725d-4b05-9c43-6b3180d7411b">INKMETRIC</a> structure that stores the display properties of the text ink object.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pim</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0082b7d3-61b2-478a-a6dd-ba59c20b7e1d">GetInkExtent Method</a>



<a href="https://msdn.microsoft.com/58774f49-6af2-4b81-bbd5-709eb694af2d">IInkLineInfo</a>



<a href="https://msdn.microsoft.com/27d56034-725d-4b05-9c43-6b3180d7411b">INKMETRIC Structure</a>



<a href="https://msdn.microsoft.com/42e16e86-fc90-4089-9ae0-9a896cbeaccc">SetFormat Method</a>
 

 

