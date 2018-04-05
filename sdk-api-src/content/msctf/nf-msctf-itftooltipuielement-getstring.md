---
UID: NF:msctf.ITfToolTipUIElement.GetString
title: ITfToolTipUIElement::GetString method
author: windows-driver-content
description: Returns the string of the tooltip.
old-location: tsf\itftooltipuielement_getstring.htm
old-project: TSF
ms.assetid: 2858a16a-7550-4e16-8872-ecfffa7d1b4e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetString method [Text Services Framework], GetString method [Text Services Framework], ITfToolTipUIElement interface, GetString,ITfToolTipUIElement.GetString, ITfToolTipUIElement, ITfToolTipUIElement interface [Text Services Framework], GetString method, ITfToolTipUIElement::GetString, msctf/ITfToolTipUIElement::GetString, tsf.itftooltipuielement_getstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfToolTipUIElement.GetString
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfToolTipUIElement::GetString method


## -description


Returns the string of the tooltip.


## -parameters




### -param pstr [out]

[out] A pointer to receive BSTR. This is the string for the tooltip.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



