---
UID: NF:ocidl.IPicture.get_hPal
title: IPicture::get_hPal method
author: windows-driver-content
description: Retrieves a copy of the palette currently used by the picture object.
old-location: com\ipicture_get_hpal.htm
old-project: com
ms.assetid: 84887cb7-05b0-44cc-9772-117a598c1b94
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IPicture, IPicture interface [COM], get_hPal method, IPicture::get_hPal, _ctrl_ipicture_get_hpal, com.ipicture_get_hpal, get_hPal method [COM], get_hPal method [COM], IPicture interface, get_hPal,IPicture.get_hPal, ocidl/IPicture::get_hPal
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
-	IPicture.get_hPal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPicture::get_hPal method


## -description


Retrieves a copy of the palette currently used by the picture object.


## -parameters




### -param phPal [out]

A pointer to a variable that receives the palette handle. The variable is set to <b>NULL</b> on failure.


## -returns



This method supports the standard return values E_FAIL and E_OUTOFMEMORY, as well as the following values.

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
The height was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This picture has no palette. The variable that <i>phpal</i> points to was set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>phPal</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If the picture object has ownership of the picture, it also has ownership of the palette and will destroy it when the object is itself destroyed. Otherwise the caller owns the palette. The <i>fOwn</i> parameter to <a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a> determines ownership. <a href="https://msdn.microsoft.com/de1847cd-ecc0-4941-9dbc-a60b8ef0b1c1">OleLoadPicture</a> sets <i>fOwn</i> to <b>TRUE</b> to indicate that the picture object owns the palette.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

