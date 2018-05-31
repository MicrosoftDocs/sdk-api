---
UID: NF:ocidl.IFont.get_Weight
title: IFont::get_Weight
author: windows-sdk-content
description: Gets the font's current Weight property.
old-location: com\ifont_get_weight.htm
old-project: com
ms.assetid: 3dad6648-752d-48f8-9267-24a5f5b0346c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IFont interface [COM],get_Weight method, IFont.get_Weight, IFont::get_Weight, _ctrl_ifont_get_weight, com.ifont_get_weight, get_Weight, get_Weight method [COM], get_Weight method [COM],IFont interface, ocidl/IFont::get_Weight
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IFont.get_Weight
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFont::get_Weight


## -description


Gets  the font's current Weight property.


## -parameters




### -param pWeight [out]

A pointer to the caller-allocated variable that receives the current Weight property for the font. For a list of possible values, see the <b>lfWeight</b> member of the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure.


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
<dt><b></b></dt>
</dl>
</td>
<td width="60%">
The weight was retrieved successfully. If the weight is indeterminate, a font object should store <b>FW_NORMAL</b> in *<i>pWeight</i> and return <b>S_OK</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b></b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pWeight</i> parameter is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/716c77f3-6224-40d7-abea-46ed5eedb08a">IFont::put_Weight</a>
 

 

