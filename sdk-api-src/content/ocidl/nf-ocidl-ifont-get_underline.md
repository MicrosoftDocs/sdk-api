---
UID: NF:ocidl.IFont.get_Underline
title: IFont::get_Underline
author: windows-sdk-content
description: Gets the font's current Underline property.
old-location: com\ifont_get_underline.htm
old-project: com
ms.assetid: 714a2678-6e3d-4b8d-8632-20eb41618fff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFont interface [COM],get_Underline method, IFont.get_Underline, IFont::get_Underline, _ctrl_ifont_get_underline, com.ifont_get_underline, get_Underline, get_Underline method [COM], get_Underline method [COM],IFont interface, ocidl/IFont::get_Underline
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
 - IFont.get_Underline
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IFont::get_Underline


## -description


Gets the font's current Underline property..


## -parameters




### -param pUnderline [out]

A pointer to the caller-allocated variable that receives the current Underline property for the font.


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
        *<i>pUnderline</i> to <b>FALSE</b> and return 
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
The address in the <i>pUnderline</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/c763c050-cf69-4c9d-83a9-66ccc1d4376c">IFont::put_Underline</a>
 

 

