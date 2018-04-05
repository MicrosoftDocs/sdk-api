---
UID: NF:ocidl.IFont.get_Bold
title: IFont::get_Bold method
author: windows-driver-content
description: Gets the font's current Bold property.
old-location: com\ifont_get_bold.htm
old-project: com
ms.assetid: bc0a8353-852b-4314-83b1-a07321159945
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IFont, IFont interface [COM], get_Bold method, IFont::get_Bold, _ctrl_ifont_get_bold, com.ifont_get_bold, get_Bold method [COM], get_Bold method [COM], IFont interface, get_Bold,IFont.get_Bold, ocidl/IFont::get_Bold
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
-	IFont.get_Bold
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IFont::get_Bold method


## -description


Gets the font's current Bold property.


## -parameters




### -param pBold [out]

A pointer to a caller-allocated 
     variable that receives the current Bold property for the font.


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
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
The state was retrieved successfully. If the state is indeterminate, a font object should set *<i>pBold</i> to <b>FALSE</b> and return <b>S_OK</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in pBold is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/c25738fe-daf4-4eac-b4b0-354950e29f27">IFont::put_Bold</a>
 

 

