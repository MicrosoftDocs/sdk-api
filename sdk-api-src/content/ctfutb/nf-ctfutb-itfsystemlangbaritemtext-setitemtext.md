---
UID: NF:ctfutb.ITfSystemLangBarItemText.SetItemText
title: ITfSystemLangBarItemText::SetItemText
author: windows-driver-content
description: The ITfSystemLangBarItemText::SetItemText method modifies the text displayed for the system language bar menu.
old-location: tsf\itfsystemlangbaritemtext_setitemtext.htm
old-project: TSF
ms.assetid: 4265f1b6-8688-4b88-b738-e373beea622b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfSystemLangBarItemText interface [Text Services Framework],SetItemText method, ITfSystemLangBarItemText.SetItemText, ITfSystemLangBarItemText::SetItemText, SetItemText, SetItemText method [Text Services Framework], SetItemText method [Text Services Framework],ITfSystemLangBarItemText interface, ctfutb/ITfSystemLangBarItemText::SetItemText, tsf.itfsystemlangbaritemtext_setitemtext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: Msctf.h
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
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfSystemLangBarItemText.SetItemText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemLangBarItemText::SetItemText


## -description


The <b>ITfSystemLangBarItemText::SetItemText</b> method modifies the text displayed for the system language bar menu.


## -parameters




### -param pch [in]

[in] A string that appears as a description.


### -param cch [in]

[in] Size, in characters, of the string.


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
A parameter is invalid.

</td>
</tr>
</table>
 



